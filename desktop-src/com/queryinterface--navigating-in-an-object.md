---
title: QueryInterface che si sposta in un oggetto
description: QueryInterface che si sposta in un oggetto
ms.assetid: 7dec015f-7609-40eb-a71e-f6e9c9b9f8ff
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3dbd44d200bf0a992f47bc375d0782bdadacf6a3
ms.sourcegitcommit: 85688bbfbe5b121bc05ddf112d54c23a469dfbc0
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "104336061"
---
# <a name="queryinterface-navigating-in-an-object"></a>QueryInterface: spostamento in un oggetto

Quando si dispone di un puntatore iniziale a un'interfaccia su un oggetto, COM dispone di un meccanismo molto semplice per verificare se l'oggetto supporta un'altra interfaccia specifica e, in caso affermativo, ottenere un puntatore. Per informazioni su come ottenere un puntatore iniziale a un'interfaccia su un oggetto, vedere [recupero di un puntatore a un oggetto](getting-a-pointer-to-an-object.md). Questo meccanismo è il metodo [**QueryInterface**](/windows/desktop/api/Unknwn/nf-unknwn-iunknown-queryinterface(q)) dell'interfaccia [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) . Se l'oggetto supporta l'interfaccia richiesta, il metodo deve restituire un puntatore a tale interfaccia. Ciò consente a un oggetto di spostarsi liberamente tra le interfacce supportate da un oggetto. **QueryInterface** separa la richiesta "si supporta un dato contratto?" dall'utilizzo a prestazioni elevate di tale contratto una volta che le negoziazioni sono state completate.

Quando un client ottiene inizialmente l'accesso a un oggetto, il client riceverà almeno un puntatore all'interfaccia [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) (l'interfaccia più fondamentale) attraverso il quale può controllare la durata dell'oggetto, indicando all'oggetto quando viene eseguita utilizzando l'oggetto, e richiamare [**QueryInterface**](/windows/desktop/api/Unknwn/nf-unknwn-iunknown-queryinterface(q)). Il client viene programmato per chiedere a ogni oggetto gestito di eseguire alcune operazioni, ma l'interfaccia **IUnknown** non dispone di funzioni per tali operazioni. Queste operazioni vengono invece espresse tramite altre interfacce. Il client viene quindi programmato per la negoziazione con gli oggetti per tali interfacce. In particolare, il client chiamerà **QueryInterface** per chiedere a un oggetto un'interfaccia tramite la quale il client può richiamare le operazioni desiderate.

Poiché l'oggetto implementa [**QueryInterface**](/windows/desktop/api/Unknwn/nf-unknwn-iunknown-queryinterface(q)), è in grado di accettare o rifiutare la richiesta. Se l'oggetto accetta la richiesta del client, **QueryInterface** restituisce al client un nuovo puntatore all'interfaccia richiesta. Tramite tale puntatore di interfaccia, il client può accedere ai metodi di tale interfaccia. Se invece l'oggetto rifiuta la richiesta del client, **QueryInterface** restituisce un puntatore null, ovvero un errore, e il client non dispone di un puntatore tramite il quale chiamare le funzioni desiderate. In questo caso, il client deve occuparsi normalmente di tale possibilità. Si supponga, ad esempio, che un client disponga di un puntatore all'interfaccia A su un oggetto e chieda le interfacce B e C. si supponga inoltre che l'oggetto supporti l'interfaccia B ma non supporti l'interfaccia C. Il risultato è che l'oggetto restituisce un puntatore a B e segnala che C non è supportato.

Un punto chiave è che quando un oggetto rifiuta una chiamata a [**QueryInterface**](/windows/desktop/api/Unknwn/nf-unknwn-iunknown-queryinterface(q)), è impossibile per il client chiedere all'oggetto di eseguire le operazioni espresse tramite l'interfaccia richiesta. Un client deve disporre di un puntatore a interfaccia per richiamare i metodi in tale interfaccia. Se l'oggetto rifiuta di fornire il puntatore richiesto, è necessario che il client sia pronto per eseguire l'operazione senza, né in alcun modo che abbia avuto intenzione di eseguire tale oggetto oppure tentando di eseguire il fallback in un'altra interfaccia, forse meno potente. Questa funzionalità della funzionalità COM funziona in modo ottimale rispetto ad altri sistemi orientati a oggetti in cui non è possibile sapere se una funzione funzionerà finché non si chiama tale funzione e anche in questo caso la gestione degli errori non è certo. **QueryInterface** fornisce un modo affidabile e coerente per sapere se un oggetto supporta un'interfaccia prima di tentare di chiamarne i metodi.

Il metodo [**QueryInterface**](/windows/desktop/api/Unknwn/nf-unknwn-iunknown-queryinterface(q)) fornisce inoltre un modo solido e affidabile per un oggetto per indicare che non supporta un determinato contratto. Ovvero, se in una chiamata a **QueryInterface** One chiede a un oggetto "obsoleto" se supporta un'interfaccia "nuova" (uno, ad esempio, che è stato inventato dopo che l'oggetto precedente era stato spedito), l'oggetto precedente sarà affidabile, senza causare un arresto anomalo, rispondere a "No". La tecnologia che lo supporta è l'algoritmo con cui vengono allocate IID. Sebbene possa sembrare un piccolo punto, è estremamente importante per l'architettura complessiva del sistema e la possibilità di richiedere elementi legacy sulle nuove funzionalità è sorprendentemente una funzionalità non presente nella maggior parte delle architetture degli oggetti.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Uso e implementazione di IUnknown](using-and-implementing-iunknown.md)
</dt> </dl>

 

 




