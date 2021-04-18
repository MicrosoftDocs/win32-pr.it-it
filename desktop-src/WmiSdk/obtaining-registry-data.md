---
description: È possibile ottenere o modificare i dati del registro di sistema utilizzando la classe WMI WMI StdRegProv e i relativi metodi.
ms.assetid: 7cba9dcb-741b-4118-9769-8830c6dc0752
ms.tgt_platform: multiple
title: Recupero dei dati del registro di sistema
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: f5468a577acedeccf4396607147428d9160b4d38
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106305574"
---
# <a name="obtaining-registry-data"></a>Recupero dei dati del registro di sistema

È possibile ottenere o modificare i dati del registro di sistema utilizzando la classe WMI [**WMI StdRegProv**](/previous-versions/windows/desktop/regprov/stdregprov) e i relativi metodi. Quando si usa l'utilità Regedit per visualizzare e modificare i valori del registro di sistema nel computer locale, **WMI StdRegProv** consente di usare uno script o un'applicazione per automatizzare tali attività nel computer locale e nei computer remoti.

[**WMI StdRegProv**](/previous-versions/windows/desktop/regprov/stdregprov) contiene i metodi per eseguire le operazioni seguenti:

-   Verificare le autorizzazioni di accesso per un utente
-   Creare, enumerare ed eliminare chiavi del registro di sistema
-   Creare, enumerare ed eliminare sottochiavi o valori denominati
-   Lettura, scrittura ed eliminazione dei valori dei dati

I dati del registro di sistema sono organizzati in base ad alberi, chiavi e sottochiavi annidati sotto una chiave di primo livello. I valori dei dati effettivi sono denominati voci o valori denominati.

Le sottostrutture includono quanto segue:

-   **HKEY \_ \_Radice delle classi** (abbreviata come **HKCR**)
-   **HKEY \_ \_utente corrente** (**HKCU**)
-   **HKEY \_ \_computer locale** (**HKLM**)
-   **\_utenti HKEY**
-   **HKEY \_ \_ configurazione corrente**

Ad esempio, nella voce del registro di sistema **HKEY** \\ **software** \\ **Microsoft** \\ **DirectX** \\ **InstalledVersion**, il sottoalbero HKEY è **software**, le sottochiavi sono **Microsoft** e **DirectX** e la voce del valore denominato è **InstalledVersion**.

Un [**RegistryKeyChangeEvent**](/previous-versions/windows/desktop/regprov/registrykeychangeevent) si verifica quando viene apportata una modifica a una chiave specifica, ma la voce non identifica il modo in cui i valori cambiano, né questo evento verrà attivato da modifiche al di sotto della chiave specificata. Per identificare le modifiche in un punto qualsiasi di una struttura di chiavi gerarchica, utilizzare [**RegistryTreeChangeEvent**](/previous-versions/windows/desktop/regprov/registrytreechangeevent), che non restituisce valori specifici o modifiche chiave che si verificano. Per ottenere una modifica del valore di una voce specifica, usare [**RegistryValueChangeEvent**](/previous-versions/windows/desktop/regprov/registryvaluechangeevent)e quindi leggere la voce per ottenere un valore baseline.

[**WMI StdRegProv**](/previous-versions/windows/desktop/regprov/stdregprov) dispone solo di metodi che possono essere chiamati da C++ o script, che è diverso dalla struttura della classe Win32.

Nell'esempio di codice riportato di seguito viene illustrato come utilizzare il metodo [**WMI StdRegProv. enumKey**](/previous-versions/windows/desktop/regprov/enumkey-method-in-class-stdregprov) per elencare tutte le sottochiavi software Microsoft presenti nella chiave del registro di sistema.

**HKEY \_ SOFTWARE del \_ computer locale** \\  \\ **Microsoft**


```VB
const HKEY_LOCAL_MACHINE = &H80000002
strComputer = "."

Set objReg=GetObject("winmgmts:{impersonationLevel=impersonate}!\\" & strComputer & "\root\default:StdRegProv")

strKeyPath = "SOFTWARE\Microsoft"
objReg.EnumKey HKEY_LOCAL_MACHINE, strKeyPath, arrSubKeys

For Each subkey In arrSubKeys
Wscript.Echo subkey
    
Next
```


```PowerShell

$HKEY_LOCAL_MACHINE = 2147483650
$strKeyPath = &quot;SOFTWARE\Microsoft&quot;

$objReg = [WMIClass]&quot;root\default:StdRegProv&quot;

$arrSubKeys = $objReg.EnumKey($HKEY_LOCAL_MACHINE, $strKeyPath)
foreach ($subKey in ($arrSubKeys.sNames))
{
    $subKey
}
```





[**WMI StdRegProv**](/previous-versions/windows/desktop/regprov/stdregprov) dispone di metodi diversi per la lettura dei diversi tipi di dati del valore della voce del registro di sistema. Se la voce contiene valori sconosciuti, è possibile chiamare [**WMI StdRegProv. EnumValues**](/previous-versions/windows/desktop/regprov/enumvalues-method-in-class-stdregprov) per elencarli. La tabella seguente elenca la corrispondenza tra i metodi **WMI StdRegProv** e i tipi di dati.



| Metodo                                                                                  | Tipo di dati           |
|-----------------------------------------------------------------------------------------|---------------------|
| [**GetBinaryValue**](/previous-versions/windows/desktop/regprov/getbinaryvalue-method-in-class-stdregprov)                 | **REG \_ binario**     |
| [**GetDWORDValue**](/previous-versions/windows/desktop/regprov/getdwordvalue-method-in-class-stdregprov)                   | **REG \_ DWORD**      |
| [**GetExpandedStringValue**](/previous-versions/windows/desktop/regprov/getexpandedstringvalue-method-in-class-stdregprov) | **REG \_ Espandi \_ SZ** |
| [**GetMultiStringValue**](/previous-versions/windows/desktop/regprov/getmultistringvalue-method-in-class-stdregprov)       | **REG \_ - \_ SZ**  |
| [**GetStringValue**](/previous-versions/windows/desktop/regprov/getstringvalue-method-in-class-stdregprov)                 | **REG \_ SZ**         |



 

La tabella seguente elenca i metodi corrispondenti per la creazione di nuove chiavi o valori o la modifica di quelli esistenti.



| Metodo                                                                                  | Tipo di dati           |
|-----------------------------------------------------------------------------------------|---------------------|
| [**SetBinaryValue**](/previous-versions/windows/desktop/regprov/setbinaryvalue-method-in-class-stdregprov)                 | **REG \_ binario**     |
| [**SetDWORDValue**](/previous-versions/windows/desktop/regprov/setdwordvalue-method-in-class-stdregprov)                   | **REG \_ DWORD**      |
| [**SetExpandedStringValue**](/previous-versions/windows/desktop/regprov/setexpandedstringvalue-method-in-class-stdregprov) | **REG \_ Espandi \_ SZ** |
| [**SetMultiStringValue**](/previous-versions/windows/desktop/regprov/setmultistringvalue-method-in-class-stdregprov)       | **REG \_ - \_ SZ**  |
| [**SetStringValue**](/previous-versions/windows/desktop/regprov/setstringvalue-method-in-class-stdregprov)                 | **REG \_ SZ**         |



 

Nell'esempio seguente viene illustrato come leggere l'elenco di origini per il registro eventi di sistema dalla chiave del registro di sistema.

**HKEY \_ Sistema \_ del** registro eventi di sistema del computer locale \\  \\  \\  \\  \\ **sistema** registro eventi

Si noti che gli elementi nel valore multistringa vengono considerati come una raccolta o una matrice.


```VB
const HKEY_LOCAL_MACHINE = &H80000002
strComputer = "."

Set objReg=GetObject("winmgmts:{impersonationLevel=impersonate}!\\" _ 
    & strComputer & "\root\default:StdRegProv")

strKeyPath = "SOFTWARE\Microsoft"
objReg.EnumKey HKEY_LOCAL_MACHINE, strKeyPath, arrSubKeys

For Each subkey In arrSubKeys
Wscript.Echo subkey
    
Next
```



Il provider del registro di sistema è ospitato in LocalService, non in LocalSystem. Per questo motivo, non è possibile ottenere informazioni in modalità remota dal sottoalbero **HKEY \_ \_ utente corrente** . Tuttavia, gli script eseguiti nel computer locale possono comunque accedere **all' \_ \_ utente corrente di HKEY**. È possibile impostare il modello di hosting su LocalSystem in un computer remoto, ma si tratta di un rischio per la sicurezza perché il registro di sistema nel computer remoto è vulnerabile ad accesso ostile. Per altre informazioni, vedere [hosting e sicurezza del provider](provider-hosting-and-security.md).

## <a name="examples"></a>Esempio

L'esempio di codice VBScript [Read a Binary Registry Value](https://Gallery.TechNet.Microsoft.Com/b0724cb2-36ed-4d0d-8b8f-428d0e3d0b82) in TechNet Gallery USA WMI per leggere un valore binario del registro di sistema.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Attività WMI: Registro di sistema](wmi-tasks--registry.md)
</dt> </dl>

 

 
