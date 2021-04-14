---
description: Recupera un'impostazione della shell globale.
ms.assetid: b9b1542c-8e25-4966-b3df-13bfbd9b28aa
title: Metodo IShellDispatch4. GetSetting (shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellDispatch4.GetSetting
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 755ee1d2bbd5026b1cc3ca165649e0fcb4ab20ed
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104977986"
---
# <a name="ishelldispatch4getsetting-method"></a>IShellDispatch4. GetSetting, metodo

Recupera un'impostazione della shell globale.

## <a name="syntax"></a>Sintassi


```JScript
retVal = IShellDispatch4.GetSetting(
  lSetting
)
```


```VB

IShellDispatch4.GetSetting( _
  ByVal lSetting As long _
) As VARIANT_BOOL
```





## <a name="parameters"></a>Parametri

<dl> <dt>

*lSetting* \[ in\]
</dt> <dd>

Tipo: **Long**

Valore che specifica l'impostazione della shell corrente da recuperare. In ogni chiamata è possibile recuperare una sola impostazione. I valori seguenti sono riconosciuti da questo metodo.

<dt>

<span id="SSF_AUTOCHECKSELECT"></span><span id="ssf_autocheckselect"></span>

<span id="SSF_AUTOCHECKSELECT"></span><span id="ssf_autocheckselect"></span>**SSF \_ AUTOCHECKSELECT** (0x00800000)


</dt> <dd>

**Windows Vista e versioni successive**. Stato dell'opzione **utilizza caselle di controllo per selezionare gli elementi** . Questa opzione viene abilitata automaticamente quando nel sistema è configurato un dispositivo di input penna.

</dd> <dt>

<span id="SSF_DESKTOPHTML"></span><span id="ssf_desktophtml"></span>

<span id="SSF_DESKTOPHTML"></span><span id="ssf_desktophtml"></span>**SSF \_ DESKTOPHTML** (0x00000200)


</dt> <dd>

Non usato.

</dd> <dt>

<span id="SSF_DONTPRETTYPATH"></span><span id="ssf_dontprettypath"></span>

<span id="SSF_DONTPRETTYPATH"></span><span id="ssf_dontprettypath"></span>**SSF \_ DONTPRETTYPATH** (0x00000800)


</dt> <dd>

Stato dell'opzione **Consenti tutti i nomi maiuscoli** . A partire da Windows Vista, questa opzione di cartella non è più disponibile.

</dd> <dt>

<span id="SSF_DOUBLECLICKINWEBVIEW"></span><span id="ssf_doubleclickinwebview"></span>

<span id="SSF_DOUBLECLICKINWEBVIEW"></span><span id="ssf_doubleclickinwebview"></span>**SSF \_ DOUBLECLICKINWEBVIEW** (0x00000080)


</dt> <dd>

Stato del **doppio clic per aprire l'opzione di un elemento (con un solo clic per la selezione)** .

</dd> <dt>

<span id="SSF_FILTER"></span><span id="ssf_filter"></span>

<span id="SSF_FILTER"></span><span id="ssf_filter"></span>**SSF \_ FILTER** (0x00010000)


</dt> <dd>

Non usato.

</dd> <dt>

<span id="SSF_HIDDENFILEEXTS"></span><span id="ssf_hiddenfileexts"></span>

<span id="SSF_HIDDENFILEEXTS"></span><span id="ssf_hiddenfileexts"></span>**SSF \_ HIDDENFILEEXTS** (0x00000004)


</dt> <dd>

Non usato.

</dd> <dt>

<span id="SSF_HIDEICONS"></span><span id="ssf_hideicons"></span>

<span id="SSF_HIDEICONS"></span><span id="ssf_hideicons"></span>**SSF \_ HIDEICONS** (0x00004000)


</dt> <dd>

Lo stato dell'icona visualizzato nella visualizzazione elenco di Esplora risorse. Se questa opzione è attiva, nessuna icona viene visualizzata nella visualizzazione elenco.

</dd> <dt>

<span id="SSF_ICONSONLY"></span><span id="ssf_iconsonly"></span>

<span id="SSF_ICONSONLY"></span><span id="ssf_iconsonly"></span>**SSF \_ ICONSONLY** (0x01000000)


</dt> <dd>

**Windows Vista e versioni successive**. Lo stato del nome visualizzato viene visualizzato nella visualizzazione elenco di Esplora risorse. Se questa opzione è attiva, le icone vengono visualizzate nella visualizzazione elenco, ma i nomi visualizzati non lo sono.

</dd> <dt>

<span id="SSF_MAPNETDRVBUTTON"></span><span id="ssf_mapnetdrvbutton"></span>

<span id="SSF_MAPNETDRVBUTTON"></span><span id="ssf_mapnetdrvbutton"></span>**SSF \_ MAPNETDRVBUTTON** (0x00001000)


</dt> <dd>

Stato del pulsante dell' **unità di rete Mostra mappa nell'opzione della barra degli strumenti** . A partire da Windows Vista, questa opzione non è più disponibile.

</dd> <dt>

<span id="SSF_NOCONFIRMRECYCLE"></span><span id="ssf_noconfirmrecycle"></span>

<span id="SSF_NOCONFIRMRECYCLE"></span><span id="ssf_noconfirmrecycle"></span>**SSF \_ NOCONFIRMRECYCLE** (0x00008000)


</dt> <dd>

Stato della finestra di dialogo di conferma dell' **eliminazione della visualizzazione** del cestino.

</dd> <dt>

<span id="SSF_NONETCRAWLING"></span><span id="ssf_nonetcrawling"></span>

<span id="SSF_NONETCRAWLING"></span><span id="ssf_nonetcrawling"></span>**SSF \_ NONETCRAWLING** (0x00100000)


</dt> <dd>

Lo stato dell'opzione **Cerca automaticamente le cartelle di rete e le stampanti** . A partire da Windows Vista, questa opzione non è più disponibile.

</dd> <dt>

<span id="SSF_SEPPROCESS"></span><span id="ssf_sepprocess"></span>

<span id="SSF_SEPPROCESS"></span><span id="ssf_sepprocess"></span>**SSF \_ SEPPROCESS** (0x00080000)


</dt> <dd>

Lo stato delle **finestre della cartella di avvio in un'opzione di processo separata** .

</dd> <dt>

<span id="SSF_SERVERADMINUI"></span><span id="ssf_serveradminui"></span>

<span id="SSF_SERVERADMINUI"></span><span id="ssf_serveradminui"></span>**SSF \_ SERVERADMINUI** (0x00000004)


</dt> <dd>

Non usato.

</dd> <dt>

<span id="SSF_SHOWALLOBJECTS"></span><span id="ssf_showallobjects"></span>

<span id="SSF_SHOWALLOBJECTS"></span><span id="ssf_showallobjects"></span>**SSF \_ SHOWALLOBJECTS** (0x00000001)


</dt> <dd>

Stato dell'opzione **file e cartelle nascosti** .

</dd> <dt>

<span id="SSF_SHOWATTRIBCOL"></span><span id="ssf_showattribcol"></span>

<span id="SSF_SHOWATTRIBCOL"></span><span id="ssf_showattribcol"></span>**SSF \_ SHOWATTRIBCOL** (0x00000100)


</dt> <dd>

Stato dell'opzione **Mostra attributi di file in visualizzazione dettagli** . A partire da Windows Vista, questa opzione non è più disponibile.

</dd> <dt>

<span id="SSF_SHOWCOMPCOLOR"></span><span id="ssf_showcompcolor"></span>

<span id="SSF_SHOWCOMPCOLOR"></span><span id="ssf_showcompcolor"></span>**SSF \_ SHOWCOMPCOLOR** (0x00000008)


</dt> <dd>

Lo stato dell'opzione **Mostra file NTFS crittografati o compressi in colore** .

</dd> <dt>

<span id="SSF_SHOWEXTENSIONS"></span><span id="ssf_showextensions"></span>

<span id="SSF_SHOWEXTENSIONS"></span><span id="ssf_showextensions"></span>**SSF \_ SHOWEXTENSIONS** (0x00000002)


</dt> <dd>

Stato dell'opzione **Nascondi estensioni per i tipi di file noti** .

</dd> <dt>

<span id="SSF_SHOWINFOTIP"></span><span id="ssf_showinfotip"></span>

<span id="SSF_SHOWINFOTIP"></span><span id="ssf_showinfotip"></span>**SSF \_ SHOWINFOTIP** (0x00002000)


</dt> <dd>

Lo stato dell'opzione **Mostra descrizione popup per cartella e elementi desktop** .

</dd> <dt>

<span id="SSF_SHOWSTARTPAGE"></span><span id="ssf_showstartpage"></span>

<span id="SSF_SHOWSTARTPAGE"></span><span id="ssf_showstartpage"></span>**SSF \_ SHOWSTARTPAGE** (0x00400000)


</dt> <dd>

Non usato.

</dd> <dt>

<span id="SSF_SHOWSUPERHIDDEN"></span><span id="ssf_showsuperhidden"></span>

<span id="SSF_SHOWSUPERHIDDEN"></span><span id="ssf_showsuperhidden"></span>**SSF \_ SHOWSUPERHIDDEN** (0x00040000)


</dt> <dd>

Stato dell'opzione **Nascondi file del sistema operativo protetti** .

</dd> <dt>

<span id="SSF_SHOWSYSFILES"></span><span id="ssf_showsysfiles"></span>

<span id="SSF_SHOWSYSFILES"></span><span id="ssf_showsysfiles"></span>**SSF \_ SHOWSYSFILES** (0x00000020)


</dt> <dd>

Stato dell'opzione **file e cartelle nascosti** . In Windows Vista e versioni successive, equivale a SSF \_ SHOWALLOBJECTS. Nelle versioni di Windows precedenti a Windows Vista, questo valore si riferisce allo stato dell'opzione non **visualizzare cartelle e file nascosti** .

</dd> <dt>

<span id="SSF_SHOWTYPEOVERLAY"></span><span id="ssf_showtypeoverlay"></span>

<span id="SSF_SHOWTYPEOVERLAY"></span><span id="ssf_showtypeoverlay"></span>**SSF \_ SHOWTYPEOVERLAY** (0x02000000)


</dt> <dd>

**Windows Vista e versioni successive**. Stato dell'icona del **file visualizzato nell'opzione anteprime** . Se questa opzione è attiva, quando un file fornisce una rappresentazione di anteprima viene applicata una sovrapposizione del tipo di file.

</dd> <dt>

<span id="SSF_SORTCOLUMNS"></span><span id="ssf_sortcolumns"></span>

<span id="SSF_SORTCOLUMNS"></span><span id="ssf_sortcolumns"></span>**SSF \_ SORTCOLUMNS** (0x00000010)


</dt> <dd>

Non usato.

</dd> <dt>

<span id="SSF_STARTPANELON"></span><span id="ssf_startpanelon"></span>

<span id="SSF_STARTPANELON"></span><span id="ssf_startpanelon"></span>**SSF \_ STARTPANELON** (0x00200000)


</dt> <dd>

Lo stato dell'opzione di visualizzazione di Windows XP, che consente di selezionare tra lo stile di Windows XP e lo stile classico. A partire da Windows Vista, questa opzione non è più disponibile.

</dd> <dt>

<span id="SSF_WEBVIEW"></span><span id="ssf_webview"></span>

<span id="SSF_WEBVIEW"></span><span id="ssf_webview"></span>**SSF \_ WebView** (0x00020000)


</dt> <dd>

Stato della **visualizzazione come opzione di visualizzazione Web**. A partire da Windows Vista, questa opzione non è più disponibile.

</dd> <dt>

<span id="SSF_WIN95CLASSIC"></span><span id="ssf_win95classic"></span>

<span id="SSF_WIN95CLASSIC"></span><span id="ssf_win95classic"></span>**SSF \_ WIN95CLASSIC** (0x00000400)


</dt> <dd>

Stato dell'opzione di **stile classico** . A partire da Windows Vista, questa opzione non è più disponibile.

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>Valore restituito

### <a name="jscript"></a>JScript

Tipo: **Variant \_ bool \** _

Impostare su _ *true** se l'impostazione esiste; in caso contrario, **false**.

### <a name="vb"></a>VB

Tipo: **Variant \_ bool \** _

Impostare su _ *true** se l'impostazione esiste; in caso contrario, **false**.

## <a name="examples"></a>Esempio

Negli esempi seguenti viene illustrato l'utilizzo di **GetSetting** per JScript, VBScript e Visual Basic.

JScript


```JScript
<script language="JavaScript">
    function fnIShellDispatch4GetSettingJ()
    {
        var objIShellDispatch4 = new ActiveXObject("Shell.Application");
        var vReturn;
        var ssfSHOWALLOBJECTS = 1;

        vReturn = objIShellDispatch4.GetSetting(ssfSHOWALLOBJECTS);
        alert(vReturn);
    }
</script>
```



VBScript


```VB
<script language="VBScript">
    function fnIShellDispatch4GetSettingVB()
        dim objIShellDispatch4
        
        set objIShellDispatch4 = CreateObject("Shell.Application")
        if (not objIShellDispatch4 is nothing) then
            dim vReturn
            dim ssfSHOWALLOBJECTS
            
            ssfSHOWALLOBJECTS = 1
            vReturn = objIShellDispatch4.GetSetting(ssfSHOWALLOBJECTS)
            alert(vReturn)
        end if
        set objIShellDispatch4 = nothing
    end function
</script>
```



Visual Basic:


```VB
Private Sub fnIShellDispatch4GetSetting()
    Dim objIShellDispatch4 As Shell
    
    Set objIShellDispatch4 = New Shell
    If (Not objIShellDispatch4 Is Nothing) Then
        Dim vReturn As Variant
        Dim ssfSHOWALLOBJECTS As Long
        
        ssfSHOWALLOBJECTS = 1
        vReturn = objIShellDispatch4.GetSetting(ssfSHOWALLOBJECTS)
        Debug.Print vReturn
    End If
    Set objIShellDispatch4 = Nothing
End Sub
```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop Windows XP\]<br/>                                                                   |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                                          |
| Intestazione<br/>                   | <dl> <dt>Shldisp. h</dt> </dl>                          |
| IDL<br/>                      | <dl> <dt>Shldisp. idl</dt> </dl>                        |
| DLL<br/>                      | <dl> <dt>Shell32.dll (versione 6,0 o successiva)</dt> </dl> |



 

 




