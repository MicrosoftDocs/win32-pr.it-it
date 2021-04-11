---
description: Un piccolo aggiornamento apporta modifiche a uno o più file di applicazione troppo piccoli per garantire la modifica del codice del prodotto.
ms.assetid: c74ef2bd-9cf5-4ec0-bfff-1fad0e17ba98
title: Aggiornamenti di piccole dimensioni
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 80ca87e825f462a98cc7fc80ad42d2b09b7931d9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104128371"
---
# <a name="small-updates"></a>Aggiornamenti di piccole dimensioni

Un piccolo aggiornamento apporta modifiche a uno o più file di applicazione troppo piccoli per garantire la modifica del codice del prodotto. Un aggiornamento di piccole dimensioni è noto anche come aggiornamento QFE (Quick Fix Engineering). Un piccolo aggiornamento non consente la riorganizzazione della struttura ad albero del componente della funzionalità.

Un piccolo aggiornamento tipico modifica solo uno o due file o una chiave del registro di sistema. Poiché un aggiornamento di piccole dimensioni modifica le informazioni nel file con estensione msi, è necessario modificare il codice del pacchetto di installazione. Il codice del pacchetto viene archiviato nella proprietà [**Riepilogo numero revisione**](revision-number-summary.md) del [flusso di informazioni di riepilogo](summary-information-stream.md).

Il codice prodotto non viene mai modificato con un piccolo aggiornamento, quindi tutte le modifiche introdotte da un piccolo aggiornamento devono essere coerenti con le linee guida descritte in [modifica del codice del prodotto](changing-the-product-code.md). Un aggiornamento richiede un [aggiornamento principale](major-upgrades.md) per modificare il [**ProductCode**](productcode.md). Se è necessario distinguere tra i prodotti senza modificare il codice del prodotto, usare un [aggiornamento secondario](minor-upgrades.md).

Per informazioni su come applicare un pacchetto di patch di aggiornamento di piccole dimensioni a un pacchetto di Windows Installer, vedere la pagina relativa alla [creazione di una patch di aggiornamento](creating-a-small-update-patch.md)di piccole dimensioni, [applicazione di piccoli aggiornamenti mediante l'applicazione di patch all'installazione locale del prodotto](applying-small-updates-by-patching-the-local-installation-of-the-product.md), [applicazione di piccoli aggiornamenti con la reinstallazione del prodotto](applying-small-updates-by-reinstalling-the-product.md)e [applicazione di piccoli aggiornamenti con l'applicazione di patch a un'immagine amministrativa](applying-small-updates-by-patching-an-administrative-image.md).

 

 



