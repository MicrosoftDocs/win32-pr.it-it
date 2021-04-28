---
description: Protezione DEP/NX
ms.assetid: 92F628E4-6106-42F7-B868-A3101C7A3F0A
title: Protezione DEP/NX
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3565460cbfd2e6b13c3c5ba6b1f0693a3d5b25ba
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108088569"
---
# <a name="depnx-protection"></a>Protezione DEP/NX

A partire da Windows Internet Explorer 7 in Windows Vista,  l'elemento del Pannello di controllo Internet include l'opzione Abilita protezione della memoria per ridurre gli attacchi online. Questa opzione è detta anche Protezione *esecuzione* programmi (DEP) o *No-Execute* (NX). Quando questa opzione è abilitata, funziona con il processore per impedire attacchi di overflow del buffer bloccando l'esecuzione di codice dalla memoria contrassegnata come non eseguibile.

In Windows Internet Explorer 8 nel sistema operativo Windows Vista con Service Pack 1 (SP1) o versione successiva, questa opzione è abilitata per impostazione predefinita. DEP/NX non protegge da tutte le vulnerabilità basate sulla memoria. Tuttavia, quando viene combinato con altre tecnologie come ASLR (Address Space Layout Randomization), consente di evitare vulnerabilità comuni di overflow del buffer in Windows Internet Explorer e i componenti aggiuntivi caricati. Non è necessaria alcuna interazione dell'utente aggiuntiva per fornire questa protezione e non vengono introdotte nuove richieste.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Correzione dei problemi di compatibilità nelle applicazioni Web tramite Visualizzazione Compatibilità](remediating-web-applications-and-add-ons.md)
</dt> </dl>

 

 



