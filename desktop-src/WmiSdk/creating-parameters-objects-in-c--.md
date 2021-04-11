---
description: 'I metodi IWbemServices:: ExecMethod o ExecMethodAsync richiedono la \_ \_ classe di sistema Parameters come contenitore in pInParams se il metodo in esecuzione contiene argomenti di input.'
ms.assetid: 17b72ceb-e730-4176-aa4d-189d0b6acc8b
ms.tgt_platform: multiple
title: Creazione di oggetti Parameters in C++
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4c200958f4ad00ced5455462e7a2909ac6a58cfd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104226953"
---
# <a name="creating-parameters-objects-in-c"></a>Creazione di oggetti Parameters in C++

I metodi [**IWbemServices:: ExecMethod**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execmethod) o [**ExecMethodAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execmethodasync) richiedono la classe di sistema [**\_ \_ Parameters**](--parameters.md) come contenitore in *pInParams* se il metodo in esecuzione contiene argomenti di input.

Nella procedura seguente viene descritto come creare un'istanza della classe di sistema [**\_ \_ Parameters**](--parameters.md) per mantenere le informazioni sui parametri.

**Per creare un'istanza di \_ \_ Parameters**

1.  Determinare il percorso della classe per la classe che contiene la definizione del metodo.
2.  Utilizzando il percorso della classe e il puntatore [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) passati da [**IWbemProviderInit:: Initialize**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemproviderinit-initialize), chiamare [**IWbemClassObject:: GetMethod**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-getmethod) per recuperare le classi di parametri di input e output.

    Il metodo [**GetMethod**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-getmethod) restituisce un puntatore [**IWbemClassObject**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemclassobject) per l'accesso a ognuna di queste classi.

3.  Utilizzando il puntatore [**IWbemClassObject**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemclassobject) per la classe output, chiamare [**IWbemClassObject:: SpawnInstance**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-spawninstance) per creare un'istanza della classe.
4.  Popolare l'istanza della classe impostando le proprietà che corrispondono ai valori di output e, se è presente un valore restituito per il metodo, la proprietà [returnValue](creating-a-method.md) .
5.  Passare di nuovo l'istanza dei [**\_ \_ parametri**](--parameters.md) al chiamante tramite il metodo [**IWbemObjectSink:: indica**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjectsink-indicate) .

Dopo che un provider di metodi ha determinato che i parametri di input sono corretti, il metodo a cui fa riferimento *strMethodName* potrebbe comunque essere superato o non riuscito. Alcuni provider di metodi generano un secondo thread per implementare il metodo in modo che l'esito positivo o negativo effettivo del metodo venga segnalato al chiamante tramite [**IWbemObjectSink:: sestatus**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjectsink-setstatus). Si noti che **IWbemObjectSink::** SetValue non riceve il codice restituito del metodo del provider. Tuttavia, riceve il codice restituito del meccanismo effettivo di restituzione della chiamata ed è utile solo per verificare se la chiamata si è verificata o se non è riuscita per motivi meccanici.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Chiamata a un metodo](calling-a-method.md)
</dt> <dt>

[**IWbemCallResult::GetResultObject**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemcallresult-getresultobject)
</dt> <dt>

[**IWbemServices:: ExecMethodAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execmethodasync)
</dt> <dt>

[**IWbemServices:: ExecMethod**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execmethod)
</dt> </dl>

 

 



