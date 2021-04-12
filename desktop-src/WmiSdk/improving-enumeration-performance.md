---
description: Le enumerazioni tendono a usare una quantità significativa di risorse di sistema.
ms.assetid: 4163e6c2-4ee3-4906-b297-618509666c90
ms.tgt_platform: multiple
title: Miglioramento delle prestazioni di enumerazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: df2554e9e1df2f2ece58f5703d6099d84acbe01c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104232627"
---
# <a name="improving-enumeration-performance"></a>Miglioramento delle prestazioni di enumerazione

Le enumerazioni tendono a usare una quantità significativa di risorse di sistema. Pertanto, è consigliabile tentare di ottimizzare il processo di enumerazione WMI se si prevede di eseguire enumerazioni in un gruppo di grandi dimensioni. Gli script possono inoltre utilizzare una query per evitare un calo delle prestazioni nelle operazioni "for each... Next" con un set di grandi dimensioni. Per ulteriori informazioni, vedere [esecuzione di query su WMI](querying-wmi.md).

Nella procedura seguente viene descritto come migliorare le prestazioni di enumerazione.

**Per migliorare le prestazioni di enumerazione**

1.  Impostare il parametro *è* per consentire a semisincrono di restituire i dati con un enumeratore che ignora ogni elemento da WMI mentre viene recapitato. Per ulteriori informazioni, vedere [chiamata a un metodo](calling-a-method.md).

    Nell'esempio di codice C++ riportato di seguito viene illustrato come utilizzare i flag **WBEM \_ \_ return \_ immediate** e **WBEM \_ flag di \_ \_ sola trasmissione** .

    `WBEM_FLAG_RETURN_IMMEDIATE | WBEM_FLAG_FORWARD_ONLY`

    In VBScript o Visual Basic usare i flag di scripting **WbemFlagReturnImmediately** e **WbemFlagForwardOnly** di [WbemFlagEnum](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemflagenum). Il valore combinato di questi flag è decimale 48.

    I flag di scripting e di parametro generano il comportamento seguente:

    -   Il **\_ flag WBEM \_ restituisce \_** il flag **wbemFlagReturnImmediately** o immediate per la richiesta del comportamento semisincrono. La chiamata per creare l'enumeratore restituisce immediatamente un risultato. È quindi possibile iniziare a attraversare il set di oggetti che si riceve.
    -   Il flag WBEM con flag di **\_ \_ \_ sola trasmissione** o flag **wbemFlagForwardOnly** richiede un enumeratore che non è possibile riavvolgere. Ovvero WMI può rilasciare un oggetto dopo la visualizzazione dell'oggetto.

    Nelle situazioni in cui l'enumerazione è di grandi dimensioni e l'applicazione è molto veloce, l'uso di enumeratori di sola trasmissione con l'elaborazione semisincrono consente a WMI di mantenere un numero molto inferiore di oggetti, aumentando in modo significativo il tempo di risposta e le prestazioni di memoria.

    Nell'esempio di codice VBScript riportato di seguito viene illustrato come effettuare una chiamata utilizzando i flag **wbemFlagReturnImmediately** e **wbemFlagForwardOnly** combinati per ottenere una raccolta di eventi da un log eventi.

    ```VB
    Set Events = GetObject("winmgmts:").ExecQuery _
         ("SELECT * FROM Win32_NTLogEvent " _
          & "WHERE Logfile = 'System'",,48)
    ```

    

2.  Quando possibile, evitare di utilizzare [**CreateInstanceEnum**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createinstanceenum) in C++ o [**SWbemServices. InstancesOf**](swbemservices-instancesof.md)e utilizzare invece **ExecQuery**.

    Il metodo **ExecQuery** esegue una query su WMI utilizzando le tecnologie di database, mentre [**CreateInstanceEnum**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createinstanceenum) o [**SWbemServices. InstancesOf**](swbemservices-instancesof.md) enumera gli oggetti WMI. In particolare, **ExecQuery** può richiedere subset specifici di dati che i metodi di enumerazione non possono.

    Poiché alcuni provider non dispongono di funzionalità di query, WMI fornisce una funzionalità di post-filtro che consente a WMI di annullare le istanze che non soddisfano le specifiche di una query. Il fatto che un particolare provider sfrutti questa funzionalità spetta all'autore del provider.

3.  Provare con diverse query per determinare ciò che offre le prestazioni migliori.

    WMI, ad esempio, elabora raramente in modo efficiente le query con clausole **where** nel formato Prop1 < "x". Al contrario, WMI elabora in genere le query nel formato KeyProp1 = "x" in modo efficiente.

Per ulteriori informazioni, vedere [enumerazione di WMI](enumerating-wmi.md).

 

 



