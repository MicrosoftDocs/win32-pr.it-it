---
description: Flag coerenti e done
ms.assetid: a641fa95-5587-4362-9869-e5c27c6dd2ce
title: Flag coerenti e done
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 56a61d1f715d06e6bfb6632b9bbb59276074c4d7
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104524370"
---
# <a name="consistent-and-done-flags"></a>Flag coerenti e done

COM+ crea sempre un oggetto di contesto prima di attivare un oggetto transazionale. L'oggetto context include informazioni correlate agli oggetti, ad esempio l'autore e il relativo identificatore di transazione. Ogni oggetto Context contiene anche un *flag coerente* e un *flag done*. Insieme a questi flag viene determinato lo stato dell'oggetto transazionale.

Il flag coerente indica che l'oggetto transazionale è coerente o incoerente. I dettagli specifici di ciò che rende coerente lo stato di un oggetto sono al programmatore. Quando una chiamata al metodo imposta questo flag su true, l'oggetto è coerente. False indica che l'oggetto è incoerente. COM+ imposta il flag su true quando crea un'istanza dell'oggetto. Un oggetto coerente è pronto per procedere con la transazione. Mentre un oggetto rimane attivo, le chiamate al metodo successive possono cambiare ripetutamente il flag coerente da true a false e viceversa.

Il flag done determina la durata di una transazione. Quando una chiamata al metodo restituisce, COM+ controlla il flag done. Se il metodo imposta questo flag su true, COM+ disattiva l'oggetto e annota il flag coerente. Quando il flag done è false, COM+ non disattiva l'oggetto né annota il flag coerente. COM+ imposta il flag done su false quando crea un'istanza dell'oggetto.

Il flag coerente esegue il cast di un voto per eseguire il commit o interrompere la transazione in cui viene eseguita e il flag done finalizza il voto. COM+ controlla il flag coerente quando il flag done è impostato su true in una chiamata al metodo return o quando l'oggetto viene disattivato. Sebbene un flag coerente di un oggetto possa essere modificato ripetutamente all'interno di ogni chiamata al metodo, solo l'ultima modifica viene conteggiata.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Gestione delle transazioni automatiche in COM+](managing-automatic-transactions-in-com-.md)
</dt> <dt>

[Impostazione dei flag coerenti e done](setting-the-consistent-and-done-flags.md)
</dt> </dl>

 

 



