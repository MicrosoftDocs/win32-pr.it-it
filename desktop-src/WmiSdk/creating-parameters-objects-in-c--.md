---
description: I metodi IWbemServices::ExecMethod o ExecMethodAsync richiedono la classe di sistema PARAMETERS come contenitore \_ in pInParams se il metodo in esecuzione ha \_ argomenti di input.
ms.assetid: 17b72ceb-e730-4176-aa4d-189d0b6acc8b
ms.tgt_platform: multiple
title: Creazione di oggetti parametri in C++
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eaa97753eab9554e402a91cfce72a6435d44298b6b68a83de96fd4beccd83bd3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119244521"
---
# <a name="creating-parameters-objects-in-c"></a>Creazione di oggetti parametri in C++

I [**metodi IWbemServices::ExecMethod**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execmethod) o [**ExecMethodAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execmethodasync) richiedono la classe di sistema [**\_ \_ PARAMETERS**](--parameters.md) come contenitore in *pInParams* se il metodo in esecuzione ha argomenti di input.

Nella procedura seguente viene descritto come creare un'istanza della classe di sistema [**\_ \_ PARAMETERS**](--parameters.md) per contenere le informazioni sui parametri.

**Per creare un'istanza di \_ \_ PARAMETERS**

1.  Determinare il percorso della classe contenente la definizione del metodo.
2.  Usando il percorso della classe e il puntatore [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) passato da [**IWbemProviderInit::Initialize,**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemproviderinit-initialize)chiamare [**IWbemClassObject::GetMethod**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-getmethod) per recuperare le classi di parametri di input e output.

    Il [**metodo GetMethod**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-getmethod) restituisce un [**puntatore IWbemClassObject**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemclassobject) per accedere a ognuna di queste classi.

3.  Usando il [**puntatore IWbemClassObject**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemclassobject) per la classe di output, chiamare [**IWbemClassObject::SpawnInstance**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-spawninstance) per creare un'istanza della classe.
4.  Popolare l'istanza della classe impostando le proprietà che corrispondono ai valori di output e, se è presente un valore restituito per il metodo, [la proprietà ReturnValue.](creating-a-method.md)
5.  Passare nuovamente [**\_ \_ l'istanza**](--parameters.md) PARAMETERS al chiamante tramite il [**metodo IWbemObjectSink::Indicate.**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjectsink-indicate)

Dopo che un provider di metodi determina che i parametri di input sono corretti, il metodo a cui *punta strMethodName* potrebbe comunque passare o avere esito negativo. Alcuni provider di metodi generano un secondo thread per implementare il metodo in modo che l'esito positivo o negativo effettivo del metodo venga segnalato al chiamante tramite [**IWbemObjectSink::SetStatus**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjectsink-setstatus). Si noti **che IWbemObjectSink::SetStatus** non riceve il codice restituito del metodo del provider. Riceve tuttavia il codice restituito del meccanismo di chiamata-restituzione effettivo ed è utile solo per verificare che la chiamata si sia verificata o che non sia riuscita per motivi meccanici.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Chiamata di un metodo](calling-a-method.md)
</dt> <dt>

[**IWbemCallResult::GetResultObject**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemcallresult-getresultobject)
</dt> <dt>

[**IWbemServices::ExecMethodAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execmethodasync)
</dt> <dt>

[**IWbemServices::ExecMethod**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execmethod)
</dt> </dl>

 

 



