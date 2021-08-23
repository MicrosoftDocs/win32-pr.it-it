---
title: Esplorazione di QueryInterface in un oggetto
description: Esplorazione di QueryInterface in un oggetto
ms.assetid: 7dec015f-7609-40eb-a71e-f6e9c9b9f8ff
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bdbb25f76f87b43f6fc4fc4d3a1a3eb65c19960942769818a83f176fc62f72c9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119611071"
---
# <a name="queryinterface-navigating-in-an-object"></a>QueryInterface: esplorazione in un oggetto

Dopo aver creato un puntatore iniziale a un'interfaccia su un oggetto, COM ha un meccanismo molto semplice per determinare se l'oggetto supporta un'altra interfaccia specifica e, in tal caso, per ottenere un puntatore a tale interfaccia. Per informazioni sul recupero di un puntatore iniziale a un'interfaccia su un oggetto, vedere Recupero di [un puntatore a un oggetto](getting-a-pointer-to-an-object.md). Questo meccanismo è il [**metodo QueryInterface**](/windows/desktop/api/Unknwn/nf-unknwn-iunknown-queryinterface(q)) dell'interfaccia [**IUnknown.**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) Se l'oggetto supporta l'interfaccia richiesta, il metodo deve restituire un puntatore a tale interfaccia. Ciò consente a un oggetto di spostarsi liberamente tra le interfacce supportate da un oggetto . **QueryInterface** separa la richiesta "Supporto di un determinato contratto?" dall'uso ad alte prestazioni di tale contratto dopo che le trattative hanno avuto esito positivo.

Quando un client ottiene inizialmente l'accesso a un oggetto, tale client riceverà almeno un puntatore a interfaccia [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) (l'interfaccia più fondamentale) tramite il quale può controllare la durata dell'oggetto, indicando all'oggetto quando viene eseguito l'uso dell'oggetto e [**richiamando QueryInterface**](/windows/desktop/api/Unknwn/nf-unknwn-iunknown-queryinterface(q)). Il client è programmato per chiedere a ogni oggetto che riesce a eseguire alcune operazioni, ma **l'interfaccia IUnknown** non ha funzioni per tali operazioni. Tali operazioni vengono invece espresse tramite altre interfacce. Il client è quindi programmato per negoziare con gli oggetti per tali interfacce. In particolare, il client chiamerà **QueryInterface** per richiedere a un oggetto un'interfaccia tramite la quale il client può richiamare le operazioni desiderate.

Poiché l'oggetto implementa [**QueryInterface**](/windows/desktop/api/Unknwn/nf-unknwn-iunknown-queryinterface(q)), può accettare o rifiutare la richiesta. Se l'oggetto accetta la richiesta del client, **QueryInterface** restituisce un nuovo puntatore all'interfaccia richiesta al client. Tramite tale puntatore a interfaccia, il client ha accesso ai metodi di tale interfaccia. Se, d'altra parte, l'oggetto rifiuta la richiesta del client, **QueryInterface** restituisce un puntatore Null, ovvero un errore, e il client non ha alcun puntatore tramite il quale chiamare le funzioni desiderate. In questo caso, il client deve gestire correttamente questa possibilità. Si supponga, ad esempio, che un client abbia un puntatore all'interfaccia A su un oggetto e chieda le interfacce B e C. Si supponga anche che l'oggetto supporti l'interfaccia B ma non supporti l'interfaccia C. Il risultato è che l'oggetto restituisce un puntatore a B e segnala che C non è supportato.

Un punto chiave è che quando un oggetto rifiuta una chiamata a [**QueryInterface**](/windows/desktop/api/Unknwn/nf-unknwn-iunknown-queryinterface(q)), non è possibile che il client chieda all'oggetto di eseguire le operazioni espresse tramite l'interfaccia richiesta. Un client deve avere un puntatore a interfaccia per richiamare i metodi in tale interfaccia. Se l'oggetto rifiuta di fornire il puntatore richiesto, il client deve essere pronto a fare a meno, non facendo ciò che intendeva fare con tale oggetto o tentando di eseguire il fall back su un'altra interfaccia, forse meno potente. Questa funzionalità COM funziona bene rispetto ad altri sistemi orientati a oggetti in cui non è possibile sapere se una funzione funzionerà fino a quando non si chiama tale funzione e anche in questo caso la gestione degli errori è incerta. **QueryInterface** fornisce un modo affidabile e coerente per sapere se un oggetto supporta un'interfaccia prima di tentare di chiamare i relativi metodi.

Il [**metodo QueryInterface**](/windows/desktop/api/Unknwn/nf-unknwn-iunknown-queryinterface(q)) fornisce anche un modo affidabile e affidabile per un oggetto per indicare che non supporta un determinato contratto. Ovvero, se in una chiamata a **QueryInterface** si chiede a un oggetto "vecchio" se supporta un'interfaccia "nuova", ad esempio una che è stata inventata dopo la spedizione dell'oggetto precedente, l'oggetto precedente risponderà in modo affidabile, senza causare un arresto anomalo, rispondendo "no". La tecnologia che lo supporta è l'algoritmo con cui vengono allocati gli ID. Sebbene possa sembrare un punto di piccole dimensioni, è estremamente importante per l'architettura complessiva del sistema e la possibilità di richiedere informazioni sugli elementi legacy sulle nuove funzionalità è, a sorpresa, una funzionalità non presente nella maggior parte delle altre architetture a oggetti.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Uso e implementazione di IUnknown](using-and-implementing-iunknown.md)
</dt> </dl>

 

 




