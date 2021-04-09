---
title: Struttura STGMEDIUM
description: Struttura STGMEDIUM
ms.assetid: ff1e1128-d228-45a6-a19d-2875b6c4e003
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 86faf52ab93bab39b8413ea2eb6381da24b643b5
ms.sourcegitcommit: 89f99926f946dc6c5ea600fb7c41f6b19ceac516
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/21/2020
ms.locfileid: "104047578"
---
# <a name="the-stgmedium-structure"></a>Struttura STGMEDIUM

Proprio come la struttura [**FORMATETC**](/windows/win32/api/objidl/ns-objidl-formatetc) rappresenta un miglioramento dell'identificatore di formato degli Appunti di Windows, pertanto la struttura [**STGMEDIUM**](/windows/win32/api/objidl/ns-objidl-ustgmedium-r1) rappresenta un miglioramento dell'handle di memoria globale usato per trasferire i dati. La struttura **STGMEDIUM** include un membro, **TYMED**, che indica il supporto da usare e un'Unione che comprende puntatori e un handle per ottenere qualsiasi valore medio specificato in **TYMED**.

La struttura [**STGMEDIUM**](/windows/win32/api/objidl/ns-objidl-ustgmedium-r1) consente a entrambe le origini dati e ai consumer di scegliere il supporto di scambio più efficiente in base al rendering. Se i dati sono talmente grandi che devono essere conservati su disco, l'origine dati può indicare un supporto basato su disco nel formato preferito, usando solo la memoria globale come backup se è l'unico mezzo che il consumer riconosce. La possibilità di usare il supporto migliore per gli scambi come impostazione predefinita migliora le prestazioni complessive dello scambio di dati tra le applicazioni. Ad esempio, se alcuni dei dati da trasferire sono già su disco, l'applicazione di origine può spostarla o copiarla in una nuova destinazione, nella stessa applicazione o in un altro, senza dover prima caricare i dati nella memoria globale. Al termine della ricezione, il consumer dei dati non deve riscriverlo sul disco.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Formati di dati e supporti di trasferimento](data-formats-and-transfer-media.md)
</dt> </dl>

 

 




