---
description: Protezione DEP/NX
ms.assetid: 92F628E4-6106-42F7-B868-A3101C7A3F0A
title: Protezione DEP/NX
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aec30b3758361cbe2ed20e67fe6792d6f76b58a7266c6de1d554afdba8a2519c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118329941"
---
# <a name="depnx-protection"></a>Protezione DEP/NX

A partire da Windows Internet Explorer 7 in Windows Vista, l'elemento  del Pannello di controllo Internet include l'opzione Abilita protezione della memoria per attenuare gli attacchi online. Questa opzione viene definita  anche Protezione esecuzione programmi (DEP) o *No-Execute* (NX). Quando questa opzione è abilitata, funziona con il processore per evitare attacchi di overflow del buffer bloccando l'esecuzione di codice dalla memoria contrassegnata come non eseguibile.

In Windows Internet Explorer 8 nel sistema operativo Windows Vista con Service Pack 1 (SP1) o versione successiva, questa opzione è abilitata per impostazione predefinita. DEP/NX non protegge da tutte le vulnerabilità basate sulla memoria. Tuttavia, quando viene combinato con altre tecnologie come la casualizzazione del layout dello spazio degli indirizzi (ASLR), consente di evitare vulnerabilità comuni di overflow del buffer in Windows Internet Explorer e i componenti aggiuntivi caricati. Non è necessaria alcuna interazione dell'utente aggiuntiva per fornire questa protezione e non vengono introdotte nuove richieste.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Risoluzione dei problemi di compatibilità nelle applicazioni Web tramite Visualizzazione Compatibilità](remediating-web-applications-and-add-ons.md)
</dt> </dl>

 

 



