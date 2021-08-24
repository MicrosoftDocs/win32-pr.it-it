---
description: Il valore della proprietà Riepilogo numero revisione nel flusso di informazioni di riepilogo deve essere modificato in un nuovo valore univoco durante la localizzazione di un database, perché il database di installazione viene modificato. Vedere Codici pacchetto.
ms.assetid: fce292c5-6702-4948-a13a-2a9ccacbd5c9
title: Aggiornamento di un flusso di informazioni di riepilogo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0d95e6a0cf09af5d4a024f707c0694d89def47abf8f731f394c55a11232bc07f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120039281"
---
# <a name="updating-a-summary-information-stream"></a>Aggiornamento di un flusso di informazioni di riepilogo

Il valore della proprietà Riepilogo [](summary-information-stream.md) [**numero**](revision-number-summary.md) revisione nel flusso di informazioni di riepilogo deve essere modificato in un nuovo valore univoco durante la localizzazione di un database, perché il database di installazione viene modificato. Vedere [Codici pacchetto](package-codes.md).

Il valore della proprietà [**Riepilogo**](template-summary.md) modello nel flusso di informazioni di riepilogo deve essere modificato nell'identificatore della lingua numerica (LANGID) della nuova lingua.

Se le stringhe di testo descrittive nel flusso di informazioni di riepilogo sono localizzate nella nuova lingua, la proprietà [**Riepilogo**](codepage-summary.md) tabella codici deve essere impostata sulla tabella codici corretta per la nuova lingua.

È possibile modificare il flusso di informazioni di riepilogo del pacchetto localizzato tramite la stessa procedura descritta in [Aggiunta di informazioni di riepilogo](adding-summary-information.md). Un esempio che illustra l'uso dei metodi di informazioni di riepilogo del database è disponibile anche in Windows Installer SDK come utilità WiSumInf.vbs. Per altre informazioni sui WiSumInf.vbs, vedere [Gestire le informazioni di riepilogo](manage-summary-information.md).

[Continua](adding-localized-resources.md)

 

 



