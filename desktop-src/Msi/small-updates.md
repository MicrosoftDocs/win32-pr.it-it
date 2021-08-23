---
description: Un piccolo aggiornamento apporta modifiche a uno o più file dell'applicazione troppo piccoli per giustificare la modifica del codice del prodotto.
ms.assetid: c74ef2bd-9cf5-4ec0-bfff-1fad0e17ba98
title: Aggiornamenti di piccole dimensioni
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 392e19507ca37cf865fab44485b93346dd1ad6cf6d81ada212acb2ec11ddb1c2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119628171"
---
# <a name="small-updates"></a>Aggiornamenti di piccole dimensioni

Un piccolo aggiornamento apporta modifiche a uno o più file dell'applicazione troppo piccoli per giustificare la modifica del codice del prodotto. Un aggiornamento di piccole dimensioni viene comunemente definito anche aggiornamento QFE (Quick Fix Engineering). Un piccolo aggiornamento non consente la riorganizzazione dell'albero dei componenti delle funzionalità.

Un tipico aggiornamento di piccole dimensioni modifica solo uno o due file o una chiave del Registro di sistema. Poiché un piccolo aggiornamento modifica le informazioni nel file .msi, è necessario modificare il codice del pacchetto di installazione. Il codice del pacchetto viene archiviato nella [**proprietà Riepilogo numero**](revision-number-summary.md) revisione del flusso di informazioni di [riepilogo](summary-information-stream.md).

Il codice del prodotto non viene mai modificato con un piccolo aggiornamento, quindi tutte le modifiche introdotte da un piccolo aggiornamento devono essere coerenti con le linee guida descritte in Modifica [del codice prodotto](changing-the-product-code.md). Un aggiornamento richiede un [aggiornamento importante per](major-upgrades.md) modificare [**ProductCode**](productcode.md). Se è necessario distinguere i prodotti senza modificare il codice del prodotto, usare un [aggiornamento secondario.](minor-upgrades.md)

Per informazioni su come applicare un pacchetto di patch di aggiornamento di piccole dimensioni a un pacchetto del programma di installazione di Windows, vedere Creazione di una patch di aggiornamento di piccole [dimensioni,](creating-a-small-update-patch.md)Applicazione di piccoli aggiornamenti tramite applicazione di patch all'installazione locale del [prodotto,](applying-small-updates-by-patching-the-local-installation-of-the-product.md)Applicazione di piccoli aggiornamenti [reinstallando](applying-small-updates-by-reinstalling-the-product.md)il prodotto e Applicazione di piccoli aggiornamenti tramite applicazione di patch a un'immagine [amministrativa](applying-small-updates-by-patching-an-administrative-image.md).

 

 



