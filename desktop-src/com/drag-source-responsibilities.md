---
title: Trascinare le responsabilità dell'origine
description: Trascinare le responsabilità dell'origine
ms.assetid: bafef0c1-f78e-424a-9ed0-07764a60b22d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 45ce91a795815148f442c19530a552cf7c843332
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/21/2020
ms.locfileid: "106300506"
---
# <a name="drag-source-responsibilities"></a>Trascinare le responsabilità dell'origine

L'origine di trascinamento è responsabile delle attività seguenti:

-   Fornire un oggetto di trasferimento dei dati per l'obiettivo di rilascio che espone le interfacce [**IDataObject**](/windows/desktop/api/ObjIdl/nn-objidl-idataobject) e [**IDropSource**](/windows/desktop/api/OleIdl/nn-oleidl-idropsource) .
-   Generazione del puntatore e feedback sull'origine.
-   Determinare quando l'operazione di trascinamento è stata annullata o si è verificata un'operazione di rilascio.
-   Esecuzione di qualsiasi azione sui dati originali causati dall'operazione DROP, ad esempio l'eliminazione dei dati o la creazione di un collegamento.

L'attività principale consiste nella creazione di un oggetto di trasferimento dei dati che espone le interfacce [**IDataObject**](/windows/desktop/api/ObjIdl/nn-objidl-idataobject) e [**IDropSource**](/windows/desktop/api/OleIdl/nn-oleidl-idropsource) . È possibile che l'origine di trascinamento non includa una copia dei dati selezionati. Questa operazione non è obbligatoria, ma consente di proteggersi da modifiche accidentali e consente al codice operativo degli Appunti di essere identico al codice di trascinamento della selezione.

Mentre è in corso un'operazione di trascinamento, l'origine di trascinamento è responsabile dell'impostazione del puntatore del mouse e, se necessario, per fornire commenti e suggerimenti sull'origine aggiuntivi all'utente. L'origine di trascinamento non può fornire commenti e suggerimenti per tenere traccia della posizione del mouse, ad eccezione del fatto che imposta effettivamente il puntatore reale (vedere la funzione [**secursor**](/windows/win32/api/winuser/nf-winuser-setcursor) ). Questa regola deve essere applicata per evitare conflitti con il feedback fornito dall'obiettivo di rilascio. Un'origine di trascinamento può anche essere un obiettivo di rilascio. Quando si rilasciano i dati, l'origine/destinazione può, ovviamente, fornire il feedback di destinazione per tenere traccia della posizione del mouse. In questo caso, tuttavia, si tratta dell'obiettivo di rilascio che tiene traccia del mouse, non dell'origine. In base ai commenti e suggerimenti offerti dall'obiettivo di rilascio, l'origine imposta un puntatore appropriato.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Trascinamento della selezione](drag-and-drop.md)
</dt> </dl>

 

 