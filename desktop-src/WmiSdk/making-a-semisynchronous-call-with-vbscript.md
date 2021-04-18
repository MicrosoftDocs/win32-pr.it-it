---
description: Fornisce funzionalità di accesso semisincrono e un esempio di codice per eseguire una chiamata al metodo semisincrono.
ms.assetid: 3eae38e8-6a63-45c0-99b0-94e25ddbc5a8
ms.tgt_platform: multiple
title: Esecuzione di una chiamata semisincrono con VBScript
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: e875a269d2cf1cd4e3b40d5c84d42ffb97dc35a5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106315197"
---
# <a name="making-a-semisynchronous-call-with-vbscript"></a>Esecuzione di una chiamata semisincrono con VBScript

Alcuni metodi WMI possono restituire raccolte di grandi dimensioni, causando l'interruzione della risposta degli script. Nello script, l'accesso semisincrono è l'impostazione predefinita e Strumentazione gestione Windows (WMI) imposta **wbemFlagReturnImmediately** per le chiamate che possono restituire raccolte di oggetti di grandi dimensioni, ad esempio i seguenti metodi [**SWbemServices**](swbemservices.md) : [**InstancesOf**](swbemservices-instancesof.md), [**SubclassesOf**](swbemservices-subclassesof.md), [**ExecQuery**](swbemservices-execquery.md), [**AssociatorsOf**](swbemservices-associatorsof.md)e [**ReferencesTo**](swbemservices-referencesto.md).

L'accesso semisincrono che **USA wbemFlagReturnImmediately** impostato nel parametro *iFlags* è anche il valore predefinito per le chiamate che possono restituire set di oggetti di grandi dimensioni per i metodi [**SWbemObject**](swbemobject.md) seguenti: [**istanze \_**](swbemobject-instances-.md), [**sottoclassi \_**](swbemobject-subclasses-.md), [**associatori \_**](swbemobject-associators-.md)e [**riferimenti \_**](swbemobject-references-.md).

Per ridurre l'utilizzo delle risorse di memoria WMI durante l'elaborazione di una raccolta di oggetti di grandi dimensioni, includere il valore di **wbemFlagForwardOnly** nel parametro *iFlags* . L'utilizzo di **wbemFlagForwardOnly** fa sì che WMI crei un enumeratore di sola trasmissione che non consente la rimozione della raccolta e l'accesso di nuovo agli elementi.

WMI Elimina la memoria per ogni oggetto perché l'istruzione **for each** elabora un oggetto. Non è possibile chiamare il metodo **count** per una raccolta quando il flag **wbemFlagForwardOnly** è stato impostato sulla chiamata che ha ottenuto la raccolta. Si noti che il parametro *iFlags* ha **wbemFlagReturnImmediately** e **wbemFlagForwardOnly** impostati per impostazione predefinita per il metodo [**SWbemServices.ExecNotificationQuery**](swbemservices-execnotificationquery.md) .

Nella procedura seguente viene descritto come utilizzare VBScript per effettuare una chiamata semisincrono.

**Per eseguire una chiamata semisincrono in VBScript**

1.  Impostare il parametro *iFlags* sul valore di [wbemFlagReturnImmediately](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemflagenum).
2.  Eseguire la normale chiamata sincrona per [**SWbemServices.ExecQuery**](swbemservices-execquery.md) o [**SWbemServices.ExecNotificationQuery**](swbemservices-execnotificationquery.md) con il valore *iFlags* .
3.  Se si desidera considerare gli oggetti restituiti dalla chiamata come raccolta, utilizzare una sintassi di enumerazione come VBScript **per ognuno** di essi. Poiché ogni oggetto viene restituito, viene elaborato come elemento successivo nella raccolta.
4.  Creare un enumeratore di sola trasmissione combinando il valore di **wbemFlagReturnImmediately** con il valore di **wbemFlagForwardOnly**. Il valore decimale di questa operazione o è 48. Queste costanti sono definite nella libreria dei tipi wbemdisp. tlb per Visual Basic. La maggior parte dei linguaggi di scripting usa il valore numerico o definisce una costante. Per ulteriori informazioni, vedere [WbemFlagEnum](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemflagenum).

Nell'esempio di codice seguente viene illustrato come eseguire una chiamata al metodo semisincrono. Per ulteriori informazioni, vedere [chiamata a un metodo](calling-a-method.md).


```VB
wbemFlagReturnImmediately = 16
wbemFlagForwardOnly = 32
IFlags = wbemFlagReturnImmediately + wbemFlagForwardOnly
WScript.Echo IFlags
Set objWMIService = GetObject("winmgmts:root\cimv2")
' Query for all the Win32_Process objects on the 
'     local computer and use forward-only enumerator
Set colProcesses = objWMIService.ExecQuery("SELECT Name FROM Win32_Process",,IFlags)
' Receive each object as it arrives
For Each objProcess in colProcesses
    WScript.Echo objProcess.Name
Next
```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Chiamata a un metodo](calling-a-method.md)
</dt> </dl>

 

 



