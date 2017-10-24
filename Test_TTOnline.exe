@echo off
cd ../astron/win32
start start_all.bat

rem Read the contents of PPYTHON_PATH into %PPYTHON_PATH%:
set /P PPYTHON_PATH=<PPYTHON_PATH

rem Get the user input:
if launcher:
    launcher.setRegistry('EXIT_PAGE', 'normal')

pollingDelay = 0.5
if launcher:
    print 'ToontownStart: Polling for game2 to finish...'
    while not launcher.getGame2Done():
        time.sleep(pollingDelay)
    print 'ToontownStart: Game2 is finished.'

print 'ToontownStart: Starting the game.'
from PandaModules import *
tempLoader = PandaLoader()
backgroundNode = tempLoader.loadSync(Filename('phase_3/models/gui/loading-background'))
import DirectGuiGlobals
print 'ToontownStart: setting default font'
import ToontownGlobals
DirectGuiGlobals.setDefaultFontFunc(ToontownGlobals.getInterfaceFont)
if launcher:
    launcher.setPandaErrorCode(7)

from ShowBaseGlobal import *
if base.win == None:
    print 'Unable to open window; aborting.'
    sys.exit()

if launcher:
    launcher.setPandaErrorCode(0)
    launcher.setPandaWindowOpen()

backgroundNodePath = aspect2d.attachNewNode(backgroundNode, 0)
backgroundNodePath.setPos(0.0, 0.0, 0.0)
backgroundNodePath.setScale(render2d, VBase3(1))
backgroundNodePath.find('**/fg').setBin('fixed', 20)
backgroundNodePath.find('**/bg').setBin('fixed', 10)
base.graphicsEngine.renderFrame()
DirectGuiGlobals.setDefaultRolloverSound(base.loadSfx('phase_3/audio/sfx/GUI_rollover.mp3'))
DirectGuiGlobals.setDefaultClickSound(base.loadSfx('phase_3/audio/sfx/GUI_create_toon_fwd.mp3'))
DirectGuiGlobals.setDefaultDialogGeom(loader.loadModelOnce('phase_3/models/gui/dialog_box_gui'))
if base.musicManagerIsValid:
    music = base.musicManager.getSound('phase_3/audio/bgm/tt_theme.mid')
    if music:
        music.setLoop(1)
        music.setVolume(0.90000000000000002)
        music.play()
    
    print 'ToontownStart: Loading default gui sounds'
    DirectGuiGlobals.setDefaultRolloverSound(base.loadSfx('phase_3/audio/sfx/GUI_rollover.mp3'))
    DirectGuiGlobals.setDefaultClickSound(base.loadSfx('phase_3/audio/sfx/GUI_create_toon_fwd.mp3'))
else:
    music = None
import ToontownLoader
tempLoaderOther = ToontownLoader.ToontownLoader(base)
base.loader = tempLoaderOther
__builtin__.loader = tempLoaderOther
from DirectGui import *
serverVersion = base.config.GetString('server-version', 'no_version_set')
print 'ToontownStart: serverVersion: ', serverVersion
version = OnscreenText(serverVersion, pos = (-1.3, -0.97499999999999998), scale = 0.059999999999999998, fg = Vec4(0, 0, 1, 0.59999999999999998), align = TextNode.ALeft)
import Localizer
loader.beginBulkLoad('init', Localizer.LoaderLabel, 138, gui = 0)
from ToonBaseGlobal import *
from MessengerGlobal import *
import ToontownClientRepository
searchPath = DSearchPath()
searchPath.appendDirectory(Filename('phase_3/etc'))
searchPath.appendDirectory(Filename.fromOsSpecific(os.path.expandvars('$TOONTOWN/src/configfiles')))
dcfile = Filename('toon.dc')
if vfs:
    found = vfs.resolveFilename(dcfile, searchPath)
else:
    found = dcfile.resolveFilename(searchPath)
if not found:
    print 'ToontownStart: Could not find toon.dc file'
    sys.exit()

tcr = ToontownClientRepository.ToontownClientRepository(dcfile, serverVersion, launcher)
tcr.music = music
del music
toonbase.initNametagGlobals()
toonbase.tcr = tcr
loader.endBulkLoad('init')
if launcher:
    toonbase.startShow(tcr, launcher.getGameServer())
else:
    toonbase.startShow(tcr)
backgroundNodePath.reparentTo(hidden)
backgroundNodePath.removeNode()
del backgroundNodePath
del backgroundNode
del tempLoader
del tempLoaderOther
version.cleanup()
del version
base.loader = toonbase.loader
__builtin__.loader = toonbase.loader
if not launcher:
    run()
 TMP="C:\Users\jjames\AppData\Local\Temp"
set DOWNLOAD_SERVER="http://download.toontown.com/english/currentVersionWIN/content"
set COMPUTERNAME="BLUEDOG"
set CHAT=""
set USERDOMAIN="BlueDog"
set BURN_AUTOPLAY="C:\Program Files (x86)\Roxio\OEM\Roxio Burn\"
set EMC_AUTOPLAY="C:\Program Files (x86)\Common Files\Roxio Shared\OEM\"
set HOMEDRIVE="C:"
set PSMODULEPATH="C:\Windows\system32\WindowsPowerShell\v1.0\Modules\"
set CHATTERBOX=""
set PROCESSOR_IDENTIFIER="Intel64 Family 6 Model 42 Stepping 7, GenuineIntel"
set CFG_PATH="."
set PROGRAMFILES="C:\Program Files (x86)"
set PROCESSOR_REVISION="2a07"
set PATH=";."
set QTJAVA="C:\Program Files (x86)\Java\jre6\lib\ext\QTJava.zip"
set SYSTEMROOT="C:\Windows"
set PROGRAMFILES(X86)="C:\Program Files (x86)"
set WINDOWS_TRACING_FLAGS="3"
set USER_TOONTOWN_ACCESS="VELVET"
set ASL.LOG="Destination=file"
set TEMP="C:\Users\jjames\AppData\Local\Temp"
set COMMONPROGRAMFILES(X86)="C:\Program Files (x86)\Common Files"
set PROCESSOR_ARCHITECTURE="x86"
set PATHEXT=".COM;.EXE;.BAT;.CMD;.VBS;.VBE;.JS;.JSE;.WSF;.WSH;.MSC"
set IS_TEST_SERVER="0"
set ALLUSERSPROFILE="C:\ProgramData"
set PLAYTOKEN=""
set WEB_ACCT_PARAMS=""
set LOCALAPPDATA="C:\Users\jjames\AppData\Local"
set ACCOUNT_SERVER="https://toontown.go.com"
set HOMEPATH="\Users\jjames"
set GAME_USERNAME="NvidiaTest"
set GAME_CHAT_ELIGIBLE="0"
set PROGRAMW6432="C:\Program Files"
set GAME_SERVER="https://gameserver-lv.toontown.com"
set USERNAME="jjames"
set LGID=""
set LOGONSERVER="\\BLUEDOG"
set COMSPEC="C:\Windows\system32\cmd.exe"
set PROGRAMDATA="C:\ProgramData"
set PYTHONPATH="."
set CLASSPATH=".;C:\Program Files (x86)\Java\jre6\lib\ext\QTJava.zip"
set __COMPAT_LAYER="ElevateCreateProcess"
set SESSIONNAME="Console"
set GAME_ADFRAME_BUTTON_1=""
set GAME_ADFRAME_BUTTON_2=""
set GAME_ADFRAME_BUTTON_3="http://toontown.go.com/toon-hq/top-toons"
set GAME_ADFRAME_BUTTON_4="http://toontown.go.com/help/players-guide/"
set GAME_ADFRAME_BUTTON_5=""
set GAME_ADFRAME_BUTTON_6="http://toontown.go.com/membership/account-management/"
set GAME_ADFRAME_BUTTON_7="http://toontown.go.com/help/report-bug"
set FP_NO_HOST_CHECK="NO"
set COMMONPROGRAMFILES="C:\Program Files (x86)\Common Files"
set GAME_DISL_ID="450926245"
set WINDOWS_TRACING_LOGFILE="C:\BVTBin\Tests\installpackage\csilogfile.log"
set DISLTOKEN="U2FsdGVkX18Zf1MrdUiNyMBzJOBuwfNloEjZ1EXf72EsiZgWMCZYVZieKeVaXeBlvzScQlfSh/UEAGB7a/EGBDifw8FjLNJMQNyXKf2cbp3lwDt9FL6Y4ehN/7e7wXghm5TwIDGBnsn6UqKLqW26ICGRReq9fKn3inKSJKXI0sGvH0DhKayDenerB5EH/KK2CoVOBLh1BUl4/w0TY9q8XTWEkUhJRH/FC68WlDLg0edziU5QSL77F7H6DOXqwo2h5csV+c6LtnBc9hhr/i3vEnEUs01xIFTzINUNf/lXeW6ETEHCJSuHPmntr+z0Tlup6k6AuHM3cBwhF4X0dgvZE8LUY3cRYZAb9n+hhJJMBklnFNIUsMbevwXQYjjw1nQOU2vRv7NlNdmGtHsV3gl4wBDtud/PQb5NWK8uqwgkNzXe/9Tx9gTKwkCN/YXYbskmfDXdS6EvYSKI/m4aclxQtUWF+SJ4JiGbUfDzG+8nryAPQemcrGxbMc7FmExhfsAt/34Z+YVtooE3zxALXj/diSF9NJ6uE2Bhf0xuSbxF9ZI3tnV/n7mWxa/Noi87SuHYYAt1AvL7y4TrcmRnMlGRrY6uPCClAzze3hHNfsF6oD3f46tiTNdg0rKBroslO7FH"
set SESSION_TOKEN=""
set RCAUTOPLAY="C:\Program Files (x86)\Roxio\OEM\Roxio Central 5\"
set OS="Windows_NT"
set SYSTEMDRIVE="C:"
set ADFRAME_125X125=""
set PUBLIC="C:\Users\Public"
set NUMBER_OF_PROCESSORS="8"
set APPDATA="C:\Users\jjames\AppData\Roaming"
set GAME_VERSION_TEXT="sv1.0.47.11"
set PROCESSOR_LEVEL="6"
set COMMONPROGRAMW6432="C:\Program Files\Common Files"
set CONFIG_CONFIG=":configpath=CFG_PATH"
set PROCESSOR_ARCHITEW6432="AMD64"
set ADFRAME_728X90=""
set WINDIR="C:\Windows"
set LOGIN_TOKEN="U2FsdGVkX18Zf1MrdUiNyMBzJOBuwfNloEjZ1EXf72EsiZgWMCZYVZieKeVaXeBlvzScQlfSh/UEAGB7a/EGBDifw8FjLNJMQNyXKf2cbp3lwDt9FL6Y4ehN/7e7wXghm5TwIDGBnsn6UqKLqW26ICGRReq9fKn3inKSJKXI0sGvH0DhKayDenerB5EH/KK2CoVOBLh1BUl4/w0TY9q8XTWEkUhJRH/FC68WlDLg0edziU5QSL77F7H6DOXqwo2h5csV+c6LtnBc9hhr/i3vEnEUs01xIFTzINUNf/lXeW6ETEHCJSuHPmntr+z0Tlup6k6AuHM3cBwhF4X0dgvZE8LUY3cRYZAb9n+hhJJMBklnFNIUsMbevwXQYjjw1nQOU2vRv7NlNdmGtHsV3gl4wBDtud/PQb5NWK8uqwgkNzXe/9Tx9gTKwkCN/YXYbskmfDXdS6EvYSKI/m4aclxQtUWF+SJ4JiGbUfDzG+8nryAPQemcrGxbMc7FmExhfsAt/34Z+YVtooE3zxALXj/diSF9NJ6uE2Bhf0xuSbxF9ZI3tnV/n7mWxa/Noi87SuHYYAt1AvL7y4TrcmRnMlGRrY6uPCClAzze3hHNfsF6oD3f46tiTNdg0rKBroslO7FH"
set USERPROFILE="C:\Users\jjames"
