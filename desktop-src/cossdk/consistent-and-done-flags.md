---
description: Flag coerenti e con completamento
ms.assetid: a641fa95-5587-4362-9869-e5c27c6dd2ce
title: Flag coerenti e con completamento
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 568b0c614c745f46d8bbcc816b65f501e02de1e0455f0b64216662ec52308213
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119954361"
---
# <a name="consistent-and-done-flags"></a>Flag coerenti e con completamento

COM+ crea sempre un oggetto di contesto prima di attivare un oggetto transazionale. L'oggetto di contesto contiene informazioni relative agli oggetti, ad esempio l'autore e l'identificatore della transazione. Ogni oggetto di contesto contiene anche un *flag coerente e* un flag *done*. Insieme questi flag determinano lo stato dell'oggetto transazionale.

Il flag coerente indica che l'oggetto transazionale è coerente o incoerente. I dettagli specifici di ciò che rende coerente lo stato di un oggetto sono a livello del programmatore. Quando una chiamata al metodo imposta questo flag su True, l'oggetto è coerente. False indica che l'oggetto è incoerente. COM+ imposta il flag su True quando crea un'istanza dell'oggetto. Un oggetto coerente è pronto per procedere con la transazione. Mentre un oggetto rimane attivo, le chiamate al metodo successive possono passare ripetutamente il flag coerente da True a False e viceversa.

Il flag done determina la durata di una transazione. Quando viene restituita una chiamata al metodo, COM+ controlla il flag done. Se il metodo imposta questo flag su True, COM+ disattiva l'oggetto e nota il flag coerente. Quando il flag done è False, COM+ non disattiva l'oggetto né nota il flag coerente. COM+ imposta il flag done su False quando crea un'istanza dell'oggetto.

Il flag coerente esegue il cast di un voto per il commit o l'interruzione della transazione in cui viene eseguita e il flag done finalizza il voto. COM+ controlla il flag coerente quando il flag done è impostato su True in una chiamata al metodo return o quando l'oggetto viene disattivato. Anche se il flag coerente di un oggetto può cambiare ripetutamente all'interno di ogni chiamata al metodo, viene conteggiato solo l'ultima modifica.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Gestione delle transazioni automatiche in COM+](managing-automatic-transactions-in-com-.md)
</dt> <dt>

[Impostazione dei flag Coerenti e Done](setting-the-consistent-and-done-flags.md)
</dt> </dl>

 

 



