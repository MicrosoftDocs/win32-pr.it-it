---
description: L'eliminazione di un'istanza è il comando Delete più comune che è probabile eseguire in WMI.
ms.assetid: 95ba3e9c-1397-41fe-a080-c03a98aafd42
ms.tgt_platform: multiple
title: Eliminazione di un'istanza
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b2229889ec4bc21ad234eb1636f264977bb3e25e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106310382"
---
# <a name="deleting-an-instance"></a>Eliminazione di un'istanza

L'eliminazione di un'istanza è il comando Delete più comune che è probabile eseguire in WMI. Come l'eliminazione di una classe, il comando effettivo è piuttosto semplice. Tuttavia, WMI viene eseguito in modo molto diverso a seconda del tipo di istanza che si desidera eliminare. Se l'istanza è statica, WMI Elimina semplicemente l'istanza dal repository WMI. Per informazioni sulla rimozione di classi e istanze dal repository WMI, vedere il comando per il preprocessore [**pragma deleteclass**](pragma-deleteclass.md) .

Se l'istanza è dinamica, WMI deve chiamare [**IWbemServices::D eleteinstanceasync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-deleteinstanceasync) nei provider responsabili delle classi seguenti:

-   Classe proprietaria dell'istanza di.
-   Ogni classe padre della classe proprietaria dell'istanza.
-   Ogni sottoclasse della classe proprietaria dell'istanza.

Il completamento dell'eliminazione dipende dalla classe non astratta più grande per l'istanza originale. Se il provider di una classe non astratta più in alto riesce a completare l'eliminazione, l'operazione ha esito positivo. Per ulteriori informazioni, vedere la sezione Osservazioni di [**IWbemServices::D eleteinstance**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-deleteinstance).

Per l' [API com per WMI](com-api-for-wmi.md) sono disponibili metodi diversi per l'eliminazione di un'istanza di e l'eliminazione di un oggetto.

Nella procedura seguente viene descritto come utilizzare C++ per eliminare un'istanza di una classe di base o di una classe derivata.

**Per eliminare un'istanza di una classe base o di una classe derivata mediante C++**

-   Chiamare i metodi [**IWbemServices::D eleteinstance**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-deleteinstance) o [**IWbemServices::D eleteinstanceasync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-deleteinstanceasync) .

    Come suggerisce il nome, [**DeleteInstanceAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-deleteinstanceasync) Elimina un'istanza in modo asincrono mentre [**DeleteInstance**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-deleteinstance) Elimina un'istanza in modo sincrono. Per usare **DeleteInstanceAsync**, è necessario implementare anche un oggetto [**IWbemObjectSink**](iwbemobjectsink.md) .

> [!Note]  
> Poiché il callback al sink potrebbe non essere restituito allo stesso livello di autenticazione richiesto dal client, è consigliabile utilizzare semisincrono anziché la comunicazione asincrona. Per ulteriori informazioni, vedere [chiamata a un metodo](calling-a-method.md).

 

L' [API di scripting per WMI](scripting-api-for-wmi.md) utilizza gli stessi metodi per eliminare un oggetto classe o un'istanza di.

Nella procedura seguente viene descritto come utilizzare VBScript per eliminare un'istanza di una classe di base o di una classe derivata.

**Per eliminare un'istanza di una classe base o di una classe derivata tramite VBScript**

-   Chiamare i metodi [**SWbemObject. Delete \_**](swbemobject-delete-.md) o [**SWbemObject. DeleteAsync \_**](swbemobject-deleteasync-.md) .

    Come suggerisce il nome, [**Delete \_**](swbemobject-delete-.md) Elimina un'istanza in modo sincrono mentre [**DeleteAsync \_**](swbemobject-deleteasync-.md) Elimina un'istanza in modo asincrono. Per ulteriori informazioni sull'eliminazione di un'istanza in modo asincrono, vedere [chiamata a un metodo](calling-a-method.md).

    Nell'esempio seguente viene descritto come eliminare un'istanza di utilizzando VBScript.

    ```VB
    Dim service

    Set service = GetObject("winmgmts:{impersonationLevel=impersonate}") 

    Set objwbemobject= service.get("")

    objwbemobject.Path_.Class = "MyNewClass" 
    objwbemobject.put_
    service.delete  "MyNewClass"
    ```

    

> [!Note]  
> Poiché il callback al sink potrebbe non essere restituito allo stesso livello di autenticazione richiesto dal client, è consigliabile utilizzare semisincrono anziché la comunicazione asincrona. Per ulteriori informazioni, vedere [chiamata a un metodo](calling-a-method.md).

 

 

 



