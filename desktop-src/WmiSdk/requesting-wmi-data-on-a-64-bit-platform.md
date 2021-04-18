---
description: Per impostazione predefinita, un'applicazione o uno script riceve i dati dal provider corrispondente quando esistono due versioni dei provider.
ms.assetid: 379d934e-e010-4a03-8dc1-121be43e4c6f
ms.tgt_platform: multiple
title: Richiesta di dati WMI in una piattaforma a 64 bit
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fd392d482f083a3c1b1dff3b90d70f1857aeebb4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106309908"
---
# <a name="requesting-wmi-data-on-a-64-bit-platform"></a>Richiesta di dati WMI in una piattaforma a 64 bit

Per impostazione predefinita, un'applicazione o uno script riceve i dati dal provider corrispondente quando esistono due versioni dei provider. Il provider a 32 bit restituisce i dati a un'applicazione a 32 bit, inclusi tutti gli script, e il provider a 64 bit restituisce i dati alle applicazioni compilate a 64 bit. Tuttavia, un'applicazione o uno script può richiedere i dati dal provider non predefinito, se esistente, inviando notifiche a WMI tramite flag per le chiamate al metodo.

## <a name="context-flags"></a>Flag di contesto

I flag di stringa **\_ \_ ProviderArchitecture** e **\_ \_ RequiredArchitecture** includono un set di valori gestiti da WMI, ma non definiti nei file di intestazione o di libreria dei tipi SDK. I valori vengono inseriti in un parametro di contesto per segnalare a WMI che deve richiedere dati dal provider non predefinito.

Di seguito sono elencati i flag e i relativi valori possibili.

<dl> <dt>

<span id="__ProviderArchitecture"></span><span id="__providerarchitecture"></span><span id="__PROVIDERARCHITECTURE"></span>**\_\_ProviderArchitecture**
</dt> <dd>

Valore intero, 32 o 64, che specifica la versione 32 bit o 64 bit.

</dd> <dt>

<span id="__RequiredArchitecture"></span><span id="__requiredarchitecture"></span><span id="__REQUIREDARCHITECTURE"></span>**\_\_RequiredArchitecture**
</dt> <dd>

Valore booleano utilizzato oltre a **\_ \_ ProviderArchitecture** per forzare il caricamento della versione del provider specificata. Se la versione non è disponibile, WMI restituisce l'errore 0x80041013, **wbemErrProviderLoadFailure** per Visual Basic e **WBEM \_ e il caricamento del provider non è \_ \_ \_ riuscito** per C++. Il valore predefinito per questo flag quando non è specificato è **false**.

</dd> </dl>

In un sistema a 64 bit con versioni affiancate di un provider, un'applicazione o uno script a 32 bit riceve automaticamente i dati dal provider a 32 bit, a meno che non vengano forniti questi flag e indichi che devono essere restituiti i dati del provider a 64 bit.

## <a name="using-the-context-flags"></a>Uso dei flag di contesto

Le applicazioni C++ possono usare l'interfaccia [**IWbemContext**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemcontext) con [**IWbemServices:: ExecMethod**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execmethod) per comunicare l'uso di un provider non predefinito a WMI.

Per la creazione di script e la Visual Basic, è necessario creare un oggetto [**SWbemNamedValueSet**](swbemnamedvalueset.md) contenente i flag per il parametro *ObjWbemNamedValueSet* di [**SWbemServices.ExecMethod**](swbemservices-execmethod.md). Per ulteriori informazioni sulla configurazione degli oggetti Parameters per questa chiamata, vedere [creazione di oggetti InParameters e analisi di oggetti OutParameters](constructing-inparameters-objects-and-parsing-outparameters-objects.md).

È possibile eseguire in modo sicuro script e applicazioni usando i flag di contesto nei sistemi operativi precedenti, perché WMI li ignora nei sistemi in cui non sono implementati. Sebbene esistano versioni a 32 bit e a 64 bit del provider del registro di sistema, si noti che esiste una sola versione del repository WMI.

## <a name="accessing-the-default-registry-hive"></a>Accesso all'hive del registro di sistema predefinito

La serie di esempi seguente usa il [provider del registro di sistema](/previous-versions/windows/desktop/regprov/system-registry-provider), che include versioni affiancate a 32 bit e a 64 bit preinstallate in sistemi operativi a 64 bit. In questi esempi, i client a 32 bit ottengono i dati restituiti dal provider dal nodo a 32 bit **HKEY \_ Local \_ Machine \\ software \\ Wow6432Node \\ Microsoft**. i client a 64 bit ottengono i dati restituiti dal provider dal nodo a 64 bit **HKEY \_ \_ computer locale \\ software \\ Microsoft \\ Logging**.

Gli script illustrano come chiamare i metodi della classe [**WMI StdRegProv**](/previous-versions/windows/desktop/regprov/stdregprov) del registro di sistema tramite [**SWbemServices.ExecMethod**](swbemservices-execmethod.md) per ottenere i dati dall'hive del registro di sistema a 32 bit.

Lo script seguente recupera i dati dal provider che corrisponde alla larghezza di bit del chiamante, in questo caso 64 bit, perché si tratta di uno script in esecuzione in Windows script host (WSH) a 64 bit. Lo script ottiene il valore dal nodo del registro di sistema a 64 bit **HKEY \_ Local \_ Machine \\ software \\ Microsoft \\ WBEM \\ CIMOM \\ Logging** invece che dal nodo 32-bit **HKEY \_ Local \_ Machine \\ software \\ Wow6432Node \\ Microsoft \\ WBEM \\ CIMOM**.


```VB
strComputer = "."
Const HKLM = &h80000002
Set objReg = Getobject("winmgmts:" _
    & "{impersonationLevel=impersonate}!\\" & strComputer _
    & "\root\default:stdregprov")
'Set up inParameters object
Set Inparams = objReg.Methods_("GetStringValue").Inparameters
Inparams.Hdefkey = HKLM
Inparams.Ssubkeyname = "Software\Microsoft\Wbem\CIMOM"
Inparams.Svaluename = "Logging"
set Outparams = objReg.ExecMethod_("GetStringValue", Inparams)

'Show output parameters object and the registry value HKLM\SOFTWARE\
WScript.Echo Outparams.GetObjectText_
WScript.Echo "WMI Logging is set to  " & Outparams.SValue
```



Se il valore di **registrazione** nell'hive predefinito è impostato su 1, l'output dello script avrà un aspetto simile al seguente:

``` syntax
instance of __PARAMETERS
{
    ReturnValue = 0;
    sValue = "1";
};
WMI Logging is set to 1
```

## <a name="example-specifically-requesting-the-32-bit-registry-hive-on-a-64-bit-computer"></a>Esempio: richiesta specifica dell'hive del registro di sistema a 32 bit in un computer a 64 bit

Il seguente esempio modificato dello script predefinito usa il flag di stringa **\_ \_ ProviderArchitecture** per richiedere l'accesso ai dati del registro di sistema a 32 bit in un computer a 64 bit. Il chiamante è connesso all'hive a 32 bit, indipendentemente dal fatto che si tratti di un'applicazione 32 o 64 bit.


```VB
strComputer = "."
Const HKLM = &h80000002
Set objCtx = CreateObject("WbemScripting.SWbemNamedValueSet")
objCtx.Add "__ProviderArchitecture", 32
Set objLocator = CreateObject("Wbemscripting.SWbemLocator")
Set objServices = objLocator.ConnectServer(strComputer,"root\default","","",,,,objCtx)
Set objStdRegProv = objServices.Get("StdRegProv") 

Set Inparams = objStdRegProv.Methods_("GetStringValue").Inparameters
Inparams.Hdefkey = HKLM
Inparams.Ssubkeyname = "Software\Microsoft\Wbem\CIMOM"
Inparams.Svaluename = "Logging"
set Outparams = objStdRegProv.ExecMethod_("GetStringValue", Inparams,,objCtx)

'show output parameters object and the registry value HKLM\SOFTWARE\
WScript.Echo Outparams.GetObjectText_
WScript.Echo "WMI Logging is set to  " & Outparams.SValue
```



## <a name="example-forcing-wmi-to-access-the-32-bit-registry-hive-on-a-64-bit-computer"></a>Esempio: forzando WMI ad accedere all'hive del registro di sistema a 32 bit in un computer a 64 bit

La seguente modifica dello script precedente aggiungendo i flag **\_ \_ ProviderArchitecture** e **\_ \_ RequiredArchitecture** al parametro context impone a WMI di caricare il provider a 32 bit e ottenere i dati a 32 bit. Se il provider non esiste, si verificherà un errore di caricamento del provider. È necessario specificare l'oggetto Context nella connessione a WMI chiamando [**SWbemLocator. ConnectServer**](swbemlocator-connectserver.md).


```VB
strComputer = "."
Const HKLM = &h80000002
Set objCtx = CreateObject("WbemScripting.SWbemNamedValueSet")
objCtx.Add "__ProviderArchitecture", 32
objCtx.Add "__RequiredArchitecture", TRUE
Set objLocator = CreateObject("Wbemscripting.SWbemLocator")
Set objServices = objLocator.ConnectServer(strComputer,"root\default","","",,,,objCtx)
Set objStdRegProv = objServices.Get("StdRegProv") 

' Use ExecMethod to call the GetStringValue method
Set Inparams = objStdRegProv.Methods_("GetStringValue").Inparameters
Inparams.Hdefkey = HKLM
Inparams.Ssubkeyname = "Software\Microsoft\Wbem\CIMOM"
Inparams.Svaluename = "Logging"
set Outparams = objStdRegProv.ExecMethod_("GetStringValue", Inparams,,objCtx)

'Show output parameters object and the registry value HKLM\SOFTWARE\
WScript.Echo Outparams.GetObjectText_
WScript.Echo "WMI Logging is set to  " & Outparams.SValue
```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Ottenere e fornire dati in un computer a 64 bit](getting-and-providing-data-on-a-64-bit-computer.md)
</dt> </dl>

 

 
