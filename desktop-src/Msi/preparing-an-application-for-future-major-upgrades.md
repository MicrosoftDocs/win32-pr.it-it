---
description: Gli autori dei pacchetti di installazione devono includere informazioni sull'aggiornamento nei file con estensione msi per garantire che il pacchetto di installazione possa sfruttare le funzionalità di aggiornamento complete disponibili con il Microsoft Windows Installer.
ms.assetid: 88bb2709-a1bf-4140-a145-ae6bee85dde1
title: Preparazione di un'applicazione per aggiornamenti principali futuri
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c1e0dc9ccbee10becc39274e91d2fedeb3707028
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106310969"
---
# <a name="preparing-an-application-for-future-major-upgrades"></a>Preparazione di un'applicazione per aggiornamenti principali futuri

Gli autori dei pacchetti di installazione devono includere informazioni sull'aggiornamento nei file con estensione msi per garantire che il pacchetto di installazione possa sfruttare le funzionalità di aggiornamento complete disponibili con il Microsoft Windows Installer.

È necessario assegnare a ogni applicazione, o gruppo di applicazioni, una proprietà [**UpgradeCode**](upgradecode.md) , una proprietà [**ProductVersion**](productversion.md) e una proprietà [**ProductLanguage**](productlanguage.md) . La proprietà [**UpgradeCode**](upgradecode.md) indica un gruppo di applicazioni correlate costituito da versioni diverse e versioni in lingue diverse dello stesso prodotto. Per ulteriori informazioni sull'utilizzo della proprietà [**UpgradeCode**](upgradecode.md) , vedere [utilizzo di un UpgradeCode](using-an-upgradecode.md).

**Preparazione di un'applicazione per aggiornamenti principali futuri**

1.  Determinare un nuovo valore del codice del pacchetto per l'applicazione. Per ulteriori informazioni sui codici dei pacchetti, vedere [codici di pacchetto](package-codes.md). Immettere il nuovo codice del pacchetto nella proprietà [**Riepilogo numero revisione**](revision-number-summary.md) del [flusso di informazioni di riepilogo](summary-information-stream.md).
2.  Determinare una nuova proprietà [**ProductCode**](productcode.md) per l'applicazione. Per ulteriori informazioni, vedere [modifica del codice del prodotto](changing-the-product-code.md) . Immettere [**ProductCode**](productcode.md) e il relativo valore nella [tabella delle proprietà](property-table.md).
3.  Determinare la versione dell'applicazione e la proprietà [**ProductVersion**](productversion.md) . Il [**ProductVersion**](productversion.md) deve aumentare con ogni nuova versione dell'applicazione. Si noti che il programma di installazione usa solo i primi tre campi della versione del prodotto. Se si include un quarto campo nella versione del prodotto, il programma di installazione ignorerà il quarto campo. Immettere [**ProductVersion**](productversion.md) e il relativo valore nella tabella delle proprietà.
4.  Determinare la lingua del pacchetto e la proprietà [**ProductLanguage**](productlanguage.md) . Il valore di questa proprietà deve essere un identificatore di lingua numerico (LANGID). Immettere [**ProductLanguage**](productlanguage.md) e il relativo valore nella [tabella delle proprietà](property-table.md). Si noti che l' [azione FindRelatedProducts](findrelatedproducts-action.md) usa la lingua restituita da [**MsiGetProductInfo**](/windows/desktop/api/Msi/nf-msi-msigetproductinfoa). Per il corretto funzionamento di FindRelatedProducts, l'autore del pacchetto deve assicurarsi che la proprietà [**ProductLanguage**](productlanguage.md) sia impostata nella tabella delle proprietà su una lingua elencata anche nella proprietà di [**Riepilogo del modello**](template-summary.md) .
5.  Se si sta creando un pacchetto di installazione per la prima versione del prodotto, usare un nuovo [**UpgradeCode**](upgradecode.md). Se il pacchetto è destinato a una versione più recente di un prodotto esistente o ha la stessa versione di un prodotto esistente in una lingua diversa, usare lo stesso [**UpgradeCode**](upgradecode.md) del prodotto esistente. Due prodotti con lo stesso [**ProductVersion**](productversion.md) e lo stesso [**ProductLanguage**](productlanguage.md) possono avere lo stesso [**UpgradeCode**](upgradecode.md), a meno che non si tratti di un [piccolo aggiornamento](small-updates.md) dell'altro.
6.  Il [**UpgradeCode**](upgradecode.md) ha il formato di un [GUID](guid.md). Immettere il GUID [**UpgradeCode**](upgradecode.md) nella tabella delle proprietà.

Per ulteriori informazioni, vedere [impedire l'installazione di un pacchetto obsoleto in una versione più recente](preventing-an-old-package-from-installing-over-a-newer-version.md).

 

 



