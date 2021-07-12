---
description: Windows Shell offre un potente set di oggetti di automazione che consentono di programmare la shell con Microsoft Visual Basic e linguaggi di scripting come Microsoft JScript (compatibile con la specifica del linguaggio ECMA 262) e Microsoft Visual Basic Scripting Edition (VBScript). È possibile usare questi oggetti per accedere a molte delle funzionalità e delle finestre di dialogo della shell. Ad esempio, è possibile accedere al file system, avviare programmi e modificare le impostazioni di sistema.
title: Oggetti della shell gestibili da script
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 09455fad-a769-42ef-83ba-b745ac819bf3
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: e8685b44d00d3f48e8de2a567218ef08c1cb5070
ms.sourcegitcommit: 822413efb4a70dd464e5db4d9e8693ef74f8132f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/09/2021
ms.locfileid: "113581779"
---
# <a name="scriptable-shell-objects"></a>Oggetti della shell gestibili da script

Windows Shell offre un potente set di oggetti di automazione che consentono di programmare la shell con Microsoft Visual Basic e linguaggi di scripting come Microsoft JScript (compatibile con la specifica del linguaggio ECMA 262) e Microsoft Visual Basic Scripting Edition (VBScript). È possibile usare questi oggetti per accedere a molte delle funzionalità e delle finestre di dialogo della shell. Ad esempio, è possibile accedere al file system, avviare programmi e modificare le impostazioni di sistema.

Questa sezione presenta gli oggetti shell gestibili da script.

-   [Versioni della shell](#shell-versions)
-   [Creazione di istanze di oggetti shell](#instantiating-shell-objects)
    -   [Associazione tardiva](#late-binding)
    -   [Elemento OBJECT HTML](#html-object-element)
-   [Oggetto shell](#shell-object)
    -   [Sicurezza](#security)
-   [Oggetti cartella](#folder-objects)

## <a name="shell-versions"></a>Versioni della shell

Molti degli oggetti shell sono diventati disponibili [nella versione 4.71](versions.md) della shell. Altri sono disponibili nella versione 5.00 e successive. La versione 5.00 è diventata disponibile con Windows 2000. La tabella seguente elenca ogni oggetto Shell nella versione della shell in cui l'oggetto è diventato disponibile.



| Versione 4.71                                            | Versione 5.00                                          |
|---------------------------------------------------------|-------------------------------------------------------|
| [**Cartella**](folder.md)                                | [**DIDiskQuotaUser**](didiskquotauser-object.md)     |
| [**FolderItemVerb**](folderitemverb.md)                | [**DiskQuotaControl**](diskquotacontrol-object.md)   |
| [**FolderItemVerbs**](folderitemverbs.md)              | [**Cartella2**](folder2-object.md)                     |
| [**Shell**](shell.md)                                  | [**FolderItem**](folderitem.md)                      |
| [**ShellFolderView**](shellfolderview.md)              | [**FolderItems**](folderitems.md)                    |
| [**ShellUIHelper**](shelluihelper.md)                  | [**FolderItems2**](folderitems2-object.md)           |
| [**ShellWindows**](shellwindows.md)                    | [**IShellDispatch2**](ishelldispatch2-object.md)     |
| [**WebViewFolderContents**](../lwef/webviewfoldercontents.md) | [**IShellLinkDual2**](ishelllinkdual2-object.md)     |
|                                                         | [**ShellFolderItem**](shellfolderitem-object.md)     |
|                                                         | [**ShellFolderViewOC**](shellfolderviewoc-object.md) |
|                                                         | [**ShellLinkObject**](shelllinkobject-object.md)     |



 

## <a name="instantiating-shell-objects"></a>Creazione di istanze di oggetti shell

Per creare un'istanza degli oggetti shell Visual Basic applicazioni con associazione anticipata, aggiungere riferimenti alle librerie seguenti nel progetto:

-   Microsoft Internet Controls (SHDocVw)
-   Controlli e automazione della shell Microsoft (Shell32)

### <a name="late-binding"></a>Associazione tardiva

È anche possibile creare un'istanza di molti oggetti shell con associazione tardiva. Questo approccio funziona nelle applicazioni Visual Basic e nello script. L'esempio seguente illustra come creare un'istanza [**dell'oggetto Shell**](shell.md) in JScript.


```
<SCRIPT LANGUAGE="JScript">
<!--
    function fnCreateShell()    
    {
        // Instantiate the Shell object and invoke its FileRun method.
        var oShell = new ActiveXObject("shell.application");
        oshell.FileRun;
    }
-->
</SCRIPT>
```



Nell'esempio seguente viene illustrato come creare un'istanza [**dell'oggetto Folder**](folder.md) in VBScript.


```
<SCRIPT LANGUAGE="VBScript">
<!--
    function fnCreateFolder()
        dim oShell    
        dim oFolder
        dim sDir

        sDir = "C:\SomePath" 
        set oShell = CreateObject("shell.application")
        set oFolder = oShell.NameSpace(sDir)  
    end function
-->  
</SCRIPT>
```



Nell'esempio precedente *sDir è* il percorso [**dell'oggetto**](folder.md) Folder. Si noti che [**i valori di enumerazione ShellSpecialFolderConstants**](/windows/desktop/api/Shldisp/ne-shldisp-shellspecialfolderconstants) non sono disponibili nello script.

Il ProgID per ogni oggetto Shell è illustrato nella tabella seguente.



| Oggetto                                                  | ProgID                                                                                  |
|---------------------------------------------------------|-----------------------------------------------------------------------------------------|
| [**DIDiskQuotaUser**](didiskquotauser-object.md)       | Microsoft.DiskQuota.1                                                                   |
| [**DiskQuotaControl**](diskquotacontrol-object.md)     | Impossibile eseguire l'associazione tardiva                                                                        |
| [**Cartella**](folder.md)                                | Guscio. Shell \_ Application.NameSpace("...")                                               |
| [**Cartella2**](folder2-object.md)                       | Guscio. Shell \_ Application.NameSpace("...")                                               |
| [**FolderItem**](folderitem.md)                        | Guscio. Shell \_ Application.NameSpace("..."). Self o Folder.Items.Item o Folder.ParseName |
| [**FolderItems**](folderitems.md)                      | Folder.Items                                                                            |
| [**FolderItems2**](folderitems2-object.md)             | Folder.Items                                                                            |
| [**FolderItemVerb**](folderitemverb.md)                | Shell.NameSpace("..."). Self.Verbs.Item()                                                |
| [**FolderItemVerbs**](folderitemverbs.md)              | FolderItem.Verbs o Shell.NameSpace("..."). Self.Verbs                                   |
| [**IShellDispatch2**](ishelldispatch2-object.md)       | Guscio. Applicazione \_ shell                                                                |
| [**IShellLinkDual2**](ishelllinkdual2-object.md)       | Shell.NameSpace("..."). Self.GetLink o Shell.NameSpace("..."). Items(). GetLink           |
| [**Shell**](shell.md)                                  | Guscio. Applicazione \_ shell                                                                |
| [**ShellFolderItem**](shellfolderitem-object.md)       | Shell.NameSpace("..."). Self o Shell.NameSpace("..."). Items()                           |
| [**ShellFolderView**](shellfolderview.md)              | Impossibile eseguire l'associazione tardiva                                                                        |
| [**ShellFolderViewOC**](shellfolderviewoc-object.md)   | Impossibile eseguire l'associazione tardiva                                                                        |
| [**ShellLinkObject**](shelllinkobject-object.md)       | Shell.NameSpace("..."). Self.GetLink o Shell.NameSpace("..."). Items(). GetLink           |
| [**ShellUIHelper**](shelluihelper.md)                  | Impossibile eseguire l'associazione tardiva                                                                        |
| [**ShellWindows**](shellwindows.md)                    | Guscio. Shell \_ Windows o ShellWindows. \_ NewEnum                                          |
| [**WebViewFolderContents**](../lwef/webviewfoldercontents.md) | Impossibile eseguire l'associazione tardiva                                                                        |



 

### <a name="html-object-element"></a>Elemento OBJECT HTML

È anche possibile usare [**l'elemento OBJECT**](https://msdn.microsoft.com/library/ms535859(v=VS.85).aspx) per creare un'istanza degli oggetti shell in una pagina HTML. A tale scopo, impostare l'attributo **ID** dell'elemento **OBJECT** sul nome della variabile che verrà utilizzata negli script e identificare l'oggetto usando il relativo numero registrato (CLASSID). Il codice HTML seguente crea un'istanza [**dell'oggetto ShellFolderItem**](shellfolderitem-object.md) usando l'elemento **OBJECT.**


```
<OBJECT ID="oShFolderItem" 
    NAME="Shell Folder Item Object"
    CLASSID="clsid:2fe352ea-fd1f-11d2-b1f4-00c04f8eeb3e">
</OBJECT>
```



La tabella seguente elenca ogni oggetto Shell e il rispettivo CLASSID.



| Oggetto shell                                           | Classid                              |
|--------------------------------------------------------|--------------------------------------|
| [**DIDiskQuotaUser**](didiskquotauser-object.md)       | 7988B571-EC89-11cf-9C00-00AA00A14F56 |
| [**DiskQuotaControl**](diskquotacontrol-object.md)     | 7988B571-EC89-11cf-9C00-00AA00A14F56 |
| [**Cartella**](folder.md)                                | TBBDE60-C3FF-11CE-8350-444553540000 |
| [**Cartella2**](folder2-object.md)                       | f0d2d8ef-3890-11d2-bf8b-00c04fb93661 |
| [**FolderItem**](folderitem.md)                        | 744129E0-CBE5-11CE-8350-444553540000 |
| [**FolderItems**](folderitems.md)                      | 744129E0-CBE5-11CE-8350-444553540000 |
| [**FolderItems2**](folderitems2-object.md)             | C94F0AD0-F363-11d2-A327-00C04F8EEC7F |
| [**FolderItemVerb**](folderitemverb.md)                | 08EC3E00-50B0-11CF-960C-0080C7F4EE85 |
| [**FolderItemVerbs**](folderitemverbs.md)              | 1F8352C0-50B0-11CF-960C-0080C7F4EE85 |
| [**IShellDispatch2**](ishelldispatch2-object.md)       | A4C6892C-3BA9-11d2-9DEA-00C04FB16162 |
| [**IShellLinkDual2**](ishelllinkdual2-object.md)       | 317EE249-F12E-11d2-B1E4-00C04F8EEB3E |
| [**Shell**](shell.md)                                  | 13709620-C279-11CE-A49E-444553540000 |
| [**ShellFolderItem**](shellfolderitem-object.md)       | 2fe352ea-fd1f-11d2-b1f4-00c04f8eeb3e |
| [**ShellFolderView**](shellfolderview.md)              | 62112AA1-EBE4-11cf-A5FB-0020AFE7292D |
| [**ShellFolderViewOC**](shellfolderviewoc-object.md)   | 4a3df050-23bd-11d2-939f-00a0c91eedba |
| [**ShellLinkObject**](shelllinkobject-object.md)       | 11219420-1768-11d1-95BE-00609797EA4F |
| [**ShellUIHelper**](shelluihelper.md)                  | 64AB4BB7-111E-11D1-8F79-00C04FC2FBE1 |
| [**ShellWindows**](shellwindows.md)                    | 9BA05972-F6A8-11CF-A442-00A0C90A8F39 |
| [**WebViewFolderContents**](../lwef/webviewfoldercontents.md) | 1820FED0-473E-11D0-A96C-00C04FD705A2 |



 

## <a name="shell-object"></a>Oggetto shell

[**L'oggetto Shell**](shell.md) rappresenta gli oggetti nella shell. È possibile usare i metodi esposti dall'oggetto Shell per:

-   Aprire, esplorare e cercare le cartelle.
-   Ridurre a icona, ripristinare, sovrapporre o affiancare le finestre aperte.
-   Avviare Pannello di controllo applicazioni.
-   Visualizzare le finestre di dialogo di sistema.

Gli utenti hanno probabilmente maggiore familiarità con i comandi a cui accedono dal menu **Start** e dal menu di scelta rapida della barra delle applicazioni. Il menu di scelta rapida della barra delle applicazioni viene visualizzato quando gli utenti fa clic con il pulsante destro del mouse sulla barra delle applicazioni. L'applicazione HTML (HTA) seguente genera una pagina iniziale con pulsanti che implementano molti [**dei**](shell.md) metodi dell'oggetto Shell. Alcuni di questi metodi implementano funzionalità nel menu **Start** e nel menu di scelta rapida della barra delle applicazioni.


```
<HTML>
<HEAD>
    <TITLE>Start Page</TITLE>
    
    <OBJECT ID="oShell"
        CLASSID="clsid:13709620-C279-11CE-A49E-444553540000">
    </OBJECT>
    
    <STYLE>
        INPUT {width: 200} 
    </STYLE>  
    
    <SCRIPT LANGUAGE="VBScript">
    <!--
        function fnStart(sMethod)
            select case sMethod
              case 0    
                  'Minimizes all windows on the desktop
                oshell.Shell_MinimizeAll
              case 1  
                  'Displays the Run dialog box
                oshell.FileRun
              case 2  
                  'Displays the Shut Down Windows dialog box
                oshell.Shell_ShutdownWindows
              case 3  
                  'Displays the Find dialog box
                oshell.Shell_FindFilesr
              case 4  
                  'Displays the Date/Time dialog box
                oshell.Shell_SetTime 
              case 5  
                  'Displays the Internet Properties dialog box
                oshell.Shell_ControlPanelItem "INETCPL.cpl"
              case 6  
                  'Explores the My Documents folder
                oshell.Shell_Explore "C:\My Documents"
              case 7  
                  'Enables user to select folder from Program Files
                oshell.Shell_BrowseForFolder 0, "My Programs", 0, "C:\Program Files" 
              case 8  
                  'Opens the Favorites folder
                oshell.Shell_Open "C:\WINDOWS\Favorites"
              case 9  
                  'Displays the Taskbar Properties dialog box
                oshell.Shell_TrayProperties
            end select  
        end function      
    -->
    </SCRIPT>
</HEAD>

<BODY>
    <H1>Start...</H1>
    <INPUT type="button" value="Edit Taskbar Properties" onclick="fnStart(9)"><br>
    <INPUT type="button" value="Open Favorites Folder" onclick="fnStart(8)"><br>
    <INPUT type="button" value="Browse Program Files" onclick="fnStart(7)"><br>
    <INPUT type="button" value="Explore My Documents" onclick="fnStart(6)"><br>
    <INPUT type="button" value="Modify Internet Properties" onclick="fnStart(5)"><br>
    <INPUT type="button" value="Set System Time" onclick="fnStart(4)"><br>
    <INPUT type="button" value="Find a File or Folder" onclick="fnStart(3)"><br>
    <INPUT type="button" value="Shut Down Windows" onclick="fnStart(2)"><br>
    <INPUT type="button" value="Run" onclick="fnStart(1)">     
    <INPUT type="button" value="Minimize All Windows" onclick="fnStart(0)">     
</BODY>
</HTML>
```



### <a name="security"></a>Sicurezza

Come applicazione, un'istanza HTA viene eseguita con un modello di sicurezza diverso rispetto a una pagina Web. **Per interagire con** una pagina Web che implementa la funzionalità degli oggetti shell, gli utenti devono abilitare l'opzione Inizializza e script per i controlli ActiveX non contrassegnati come sicuri per l'area di sicurezza in cui visualizzano la pagina.

## <a name="folder-objects"></a>Oggetti cartella

[**L'oggetto Folder**](folder.md) rappresenta una cartella shell. È possibile usare i metodi esposti dall'oggetto Folder per:

-   Ottenere informazioni su una cartella.
-   Creare sottocartelle.
-   Copiare e spostare gli oggetti file nella cartella .

[**L'oggetto FolderItem**](folderitem.md) rappresenta un elemento in una cartella shell. Le relative proprietà consentono di recuperare informazioni sull'elemento. È possibile usare i metodi esposti da questo oggetto per eseguire i verbi di un elemento o per recuperare informazioni sull'oggetto [**FolderItemVerbs di un**](folderitemverbs.md) elemento.

[**L'oggetto FolderItems**](folderitems.md) rappresenta una raccolta di elementi in una cartella shell. I relativi metodi e proprietà consentono di recuperare informazioni sulla raccolta.

Nell'Visual Basic seguente viene illustrata la relazione tra diversi oggetti cartella e il modo in cui possono essere usati insieme. Quando l'utente fa clic sul pulsante di comando **denominato cmdGetPath**, il programma visualizza una finestra di dialogo che consente all'utente di selezionare una cartella da Computer locale , **dove** ssfDRIVES è il valore di enumerazione [**ShellSpecialFolderConstants**](/windows/desktop/api/Shldisp/ne-shldisp-shellspecialfolderconstants) per **Computer locale**. Quando l'utente sceglie una cartella, il percorso della cartella viene visualizzato nella casella di testo denominata **txtPath**.


```
Private Sub cmdGetPath_Click()
    Dim oShell As New Shell
    Dim oFolder As Folder
    Dim oFolderItem As FolderItem
 
    Set oFolder = oshell.Shell_BrowseForFolder(Me.hWnd, "Select a Folder", 0, ssfDrives)
   
    Set oFolderItem = oFolderItems.Item

    txtPath.Text = oFolderItem.Path
End Sub
```



In VBScript questa funzione è leggermente diversa perché i valori di enumerazione [**ShellSpecialFolderConstants**](/windows/desktop/api/Shldisp/ne-shldisp-shellspecialfolderconstants) non sono disponibili nello script. Nell'esempio seguente viene illustrato l'equivalente VBScript dell'esempio precedente.


```
<SCRIPT LANGUAGE="VBScript">
<!--
    function fnGetMyPathVB() 
        dim oShell
        dim oFolder
        dim oFolderItem
        
        set oShell = CreateObject("shell.application")      
        set oFolder = oshell.Shell_BrowseForFolder(0, "Choose a Folder", 0)             
        set oFolderItem = oFolder.Items.Item         
        
        document.all.item("myPath").innerText = oFolderItem.Path                                
    end function
-->
</SCRIPT>
```



Nell'esempio JScript seguente, che è una traduzione diretta dell'esempio di VBScript precedente, si noti come le parentesi vuote '()' vengono usate per richiamare i metodi [**Items**](folder-items.md) [**e Item.**](folderitems-item.md)


```
<SCRIPT LANGUAGE="JavaScript">
<!--
    function fnGetMyPathJ() 
    {       
        var oShell = new ActiveXObject("shell.application");
                    
        var oFolder = new Object;                   
        oFolder = oshell.Shell_BrowseForFolder(0, "Choose a folder", 0);
                                
        var oFolderItem = new Object;       
        oFolderItem = oFolder.Items().Item();                               
        
        document.all.item("myPath").innerText = oFolderItem.Path;
    }    
-->
</SCRIPT>
```



 

 
