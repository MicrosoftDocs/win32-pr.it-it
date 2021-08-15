---
description: È possibile ottenere o modificare i dati del Registro di sistema usando la classe WMI StdRegProv e i relativi metodi.
ms.assetid: 7cba9dcb-741b-4118-9769-8830c6dc0752
ms.tgt_platform: multiple
title: Recupero dei dati del Registro di sistema
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: b904316809a6949c6897e32127f85569e3b2ac13cb769db4739e61c164aa19fc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119050639"
---
# <a name="obtaining-registry-data"></a>Recupero dei dati del Registro di sistema

È possibile ottenere o modificare i dati del Registro di sistema usando la classe [**WMI StdRegProv**](/previous-versions/windows/desktop/regprov/stdregprov) e i relativi metodi. Mentre si usa l'utilità Regedit per visualizzare e modificare i valori del Registro di sistema nel computer locale, **StdRegProv** consente di usare uno script o un'applicazione per automatizzare tali attività nel computer locale e nei computer remoti.

[**StdRegProv contiene**](/previous-versions/windows/desktop/regprov/stdregprov) metodi per eseguire le operazioni seguenti:

-   Verificare le autorizzazioni di accesso per un utente
-   Creare, enumerare ed eliminare chiavi del Registro di sistema
-   Creare, enumerare ed eliminare sottochiavi o valori denominati
-   Leggere, scrivere ed eliminare valori di dati

I dati del Registro di sistema sono organizzati in base a sottoalberi, chiavi e sottochiavi annidati in una chiave di primo livello. I valori dei dati effettivi sono denominati voci o valori denominati.

I sottoalberi includono quanto segue:

-   **HKEY \_ CLASSES \_ ROOT** (abbreviato in **HKCR)**
-   **HKEY \_ CURRENT \_ USER** (**HKCU**)
-   **HKEY \_ COMPUTER \_ LOCALE** (**HKLM**)
-   **UTENTI \_ HKEY**
-   **HKEY \_ CURRENT \_ CONFIG**

Ad esempio, nella voce del Registro di sistema **HKEY** \\ **SOFTWARE** \\ **Microsoft** \\ **DirectX** \\ **InstalledVersion**  ,   il sottoalbero HKEY è SOFTWARE; le sottochiavi sono Microsoft e DirectX e la voce del valore denominato è InstalledVersion .

Un [**oggetto RegistryKeyChangeEvent**](/previous-versions/windows/desktop/regprov/registrykeychangeevent) si verifica quando si verifica una modifica a una chiave specifica, ma la voce non identifica il modo in cui i valori cambiano né questo evento verrà attivato dalle modifiche al di sotto della chiave specificata. Per identificare le modifiche in qualsiasi punto di una struttura di chiavi gerarchica, usare [**RegistryTreeChangeEvent**](/previous-versions/windows/desktop/regprov/registrytreechangeevent), che non restituisce valori specifici o modifiche di chiave che si verificano. Per ottenere una modifica del valore di una voce specifica, usare [**RegistryValueChangeEvent**](/previous-versions/windows/desktop/regprov/registryvaluechangeevent)e quindi leggere la voce per ottenere un valore di base.

[**StdRegProv**](/previous-versions/windows/desktop/regprov/stdregprov) ha solo metodi che possono essere chiamati da C++ o da uno script, che è diverso dalla struttura di classi Win32.

Nell'esempio di codice seguente viene illustrato come usare il [**metodo StdRegProv.EnumKey**](/previous-versions/windows/desktop/regprov/enumkey-method-in-class-stdregprov) per elencare tutte le sottochiavi software Microsoft nella chiave del Registro di sistema.

**HKEY \_ SOFTWARE \_ DEL COMPUTER** \\ **LOCALE** \\ **Microsoft**


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





[**StdRegProv offre**](/previous-versions/windows/desktop/regprov/stdregprov) metodi diversi per la lettura dei vari tipi di dati dei valori delle voci del Registro di sistema. Se la voce ha valori sconosciuti, è possibile chiamare [**StdRegProv.EnumValues**](/previous-versions/windows/desktop/regprov/enumvalues-method-in-class-stdregprov) per elencarli. La tabella seguente elenca la corrispondenza tra **i metodi StdRegProv** e i tipi di dati.



| Metodo                                                                                  | Tipo di dati           |
|-----------------------------------------------------------------------------------------|---------------------|
| [**GetBinaryValue**](/previous-versions/windows/desktop/regprov/getbinaryvalue-method-in-class-stdregprov)                 | **REG \_ BINARY**     |
| [**GetDWORDValue**](/previous-versions/windows/desktop/regprov/getdwordvalue-method-in-class-stdregprov)                   | **REG \_ DWORD**      |
| [**GetExpandedStringValue**](/previous-versions/windows/desktop/regprov/getexpandedstringvalue-method-in-class-stdregprov) | **REG \_ EXPAND \_ SZ** |
| [**GetMultiStringValue**](/previous-versions/windows/desktop/regprov/getmultistringvalue-method-in-class-stdregprov)       | **REG \_ MULTI \_ SZ**  |
| [**GetStringValue**](/previous-versions/windows/desktop/regprov/getstringvalue-method-in-class-stdregprov)                 | **REG \_ SZ**         |



 

Nella tabella seguente sono elencati i metodi corrispondenti per la creazione di nuove chiavi o valori o la modifica di quelli esistenti.



| Metodo                                                                                  | Tipo di dati           |
|-----------------------------------------------------------------------------------------|---------------------|
| [**SetBinaryValue**](/previous-versions/windows/desktop/regprov/setbinaryvalue-method-in-class-stdregprov)                 | **REG \_ BINARY**     |
| [**SetDWORDValue**](/previous-versions/windows/desktop/regprov/setdwordvalue-method-in-class-stdregprov)                   | **REG \_ DWORD**      |
| [**SetExpandedStringValue**](/previous-versions/windows/desktop/regprov/setexpandedstringvalue-method-in-class-stdregprov) | **REG \_ EXPAND \_ SZ** |
| [**SetMultiStringValue**](/previous-versions/windows/desktop/regprov/setmultistringvalue-method-in-class-stdregprov)       | **REG \_ MULTI \_ SZ**  |
| [**SetStringValue**](/previous-versions/windows/desktop/regprov/setstringvalue-method-in-class-stdregprov)                 | **REG \_ SZ**         |



 

Nell'esempio seguente viene illustrato come leggere l'elenco di origini per il registro eventi di sistema dalla chiave del Registro di sistema.

**HKEY \_ LOCAL \_ MACHINE** \\ **SYSTEM Current** Control \\ **Set** \\ **Services** \\ **Eventlog** \\ **System**

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



Il provider del Registro di sistema è ospitato in LocalService, non in LocalSystem. Pertanto, non è possibile ottenere informazioni in remoto dal sottoalbero **HKEY \_ CURRENT \_ USER.** Tuttavia, gli script eseguiti nel computer locale possono comunque accedere **a HKEY \_ CURRENT \_ USER**. È possibile impostare il modello di hosting su LocalSystem in un computer remoto, ma questo è un rischio per la sicurezza perché il Registro di sistema nel computer remoto è vulnerabile ad accesso ostile. Per altre informazioni, vedere [Provider Hosting and Security](provider-hosting-and-security.md).

## <a name="examples"></a>Esempio

L'esempio di codice VBScript Read [a Binary Registry Value](https://Gallery.TechNet.Microsoft.Com/b0724cb2-36ed-4d0d-8b8f-428d0e3d0b82) in TechNet Gallery usa WMI per leggere un valore binario del Registro di sistema.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Attività WMI: Registro di sistema](wmi-tasks--registry.md)
</dt> </dl>

 

 
