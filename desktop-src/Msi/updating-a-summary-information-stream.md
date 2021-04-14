---
description: Il valore della proprietà riepilogo Numero revisione nel flusso di informazioni di riepilogo deve essere modificato in un nuovo valore univoco durante la localizzazione di un database, perché è in corso la modifica del database di installazione. Vedere codici di pacchetto.
ms.assetid: fce292c5-6702-4948-a13a-2a9ccacbd5c9
title: Aggiornamento di un flusso di informazioni di riepilogo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 37c022023f79d8f4d3999db6e11e4cf65b73e1ac
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104401785"
---
# <a name="updating-a-summary-information-stream"></a>Aggiornamento di un flusso di informazioni di riepilogo

Il valore della proprietà [**Riepilogo numero revisione**](revision-number-summary.md) nel flusso di [informazioni di riepilogo](summary-information-stream.md) deve essere modificato in un nuovo valore univoco durante la localizzazione di un database, perché è in corso la modifica del database di installazione. Vedere [codici di pacchetto](package-codes.md).

Il valore della proprietà di [**Riepilogo del modello**](template-summary.md) nel flusso di informazioni di riepilogo deve essere modificato in LangID (numeric Language Identifier) del nuovo linguaggio.

Se le stringhe di testo descrittivo nel flusso di informazioni di riepilogo sono localizzate nel nuovo linguaggio, è necessario impostare la proprietà di [**Riepilogo codepage**](codepage-summary.md) sulla tabella codici corretta per il nuovo linguaggio.

È possibile modificare il flusso di informazioni di riepilogo del pacchetto localizzato con la stessa procedura descritta in [aggiunta di informazioni di riepilogo](adding-summary-information.md). Un esempio che illustra l'uso dei metodi di informazioni di riepilogo del database viene fornito anche in Windows Installer SDK come WiSumInf.vbs di utilità. Per ulteriori informazioni su WiSumInf.vbs, vedere [gestione delle informazioni di riepilogo](manage-summary-information.md).

[Continua](adding-localized-resources.md)

 

 



