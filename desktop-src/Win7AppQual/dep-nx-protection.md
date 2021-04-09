---
description: .
ms.assetid: 92F628E4-6106-42F7-B868-A3101C7A3F0A
title: Protezione DEP/NX
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 61c4a4cedead32504b6b78ba34bb72ee6b2ef400
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103885398"
---
# <a name="depnx-protection"></a>Protezione DEP/NX

A partire da Windows Internet Explorer 7 in Windows Vista, l'elemento del pannello di controllo Internet include un'opzione **Abilita protezione della memoria** che consente di attenuare gli attacchi online. Questa opzione è definita anche protezione *esecuzione* programmi (DEP) o *No-Execute* (NX). Quando questa opzione è abilitata, funziona con il processore per prevenire gli attacchi di overflow del buffer bloccando l'esecuzione del codice dalla memoria contrassegnata come non eseguibile.

In Windows Internet Explorer 8 sul sistema operativo Windows Vista con Service Pack 1 (SP1) o versione successiva questa opzione è abilitata per impostazione predefinita. DEP/NX non protegge da tutte le vulnerabilità basate sulla memoria. Tuttavia, quando è combinato con altre tecnologie come la sequenza di ASLR (Address Space Layout), consente di evitare vulnerabilità comuni di overflow del buffer in Windows Internet Explorer e i componenti aggiuntivi caricati. Non è necessaria alcuna interazione con l'utente aggiuntiva per fornire questa protezione e non vengono introdotti nuovi messaggi di richiesta.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Correzione dei problemi di compatibilità nelle applicazioni Web utilizzando visualizzazione compatibilità](remediating-web-applications-and-add-ons.md)
</dt> </dl>

 

 



