---
description: Gli autori dei pacchetti di installazione devono includere le informazioni di aggiornamento nei file .msi per assicurarsi che il pacchetto di installazione possa sfruttare le funzionalità di aggiornamento complete disponibili con il programma di installazione di Microsoft Windows.
ms.assetid: 88bb2709-a1bf-4140-a145-ae6bee85dde1
title: Preparazione di un'applicazione per gli aggiornamenti principali futuri
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0c38adc97fce578b48bc721b4265696486351097771cf936efc1e667752a7a36
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118377352"
---
# <a name="preparing-an-application-for-future-major-upgrades"></a>Preparazione di un'applicazione per gli aggiornamenti principali futuri

Gli autori dei pacchetti di installazione devono includere le informazioni di aggiornamento nei file .msi per assicurarsi che il pacchetto di installazione possa sfruttare le funzionalità di aggiornamento complete disponibili con il programma di installazione di Microsoft Windows.

A ogni applicazione o gruppo di applicazioni devono essere assegnate una [**proprietà UpgradeCode,**](upgradecode.md) [**una proprietà ProductVersion**](productversion.md) e una proprietà [**ProductLanguage.**](productlanguage.md) La [**proprietà UpgradeCode**](upgradecode.md) indica una famiglia di applicazioni correlate costituite da versioni diverse e versioni in lingue diverse dello stesso prodotto. Per altre informazioni sull'uso [**della proprietà UpgradeCode,**](upgradecode.md) vedere [Uso di UpgradeCode.](using-an-upgradecode.md)

**Preparazione di un'applicazione per gli aggiornamenti principali futuri**

1.  Determinare un nuovo valore del codice del pacchetto per l'applicazione. Per altre informazioni sui codici dei pacchetti, vedere [Codici dei pacchetti.](package-codes.md) Immettere il nuovo codice del pacchetto nella [**proprietà Riepilogo numero revisione**](revision-number-summary.md) del flusso di informazioni di [riepilogo](summary-information-stream.md).
2.  Determinare una [**nuova proprietà ProductCode**](productcode.md) per l'applicazione. Per [altre informazioni, vedere Modifica del](changing-the-product-code.md) codice prodotto. Immettere [**ProductCode**](productcode.md) e il relativo valore nella [tabella Proprietà](property-table.md).
3.  Determinare la versione dell'applicazione e la [**proprietà ProductVersion.**](productversion.md) ProductVersion [**deve**](productversion.md) aumentare con ogni nuova versione dell'applicazione. Si noti che il programma di installazione usa solo i primi tre campi della versione del prodotto. Se si include un quarto campo nella versione del prodotto, il programma di installazione ignora il quarto campo. Immettere [**ProductVersion**](productversion.md) e il relativo valore nella tabella Proprietà.
4.  Determinare la lingua del pacchetto e la [**proprietà ProductLanguage.**](productlanguage.md) Il valore di questa proprietà deve essere un identificatore di lingua numerico (LANGID). Immettere [**ProductLanguage**](productlanguage.md) e il relativo valore nella [tabella Proprietà](property-table.md). Si noti che [l'azione FindRelatedProducts](findrelatedproducts-action.md) usa la lingua restituita [**da MsiGetProductInfo.**](/windows/desktop/api/Msi/nf-msi-msigetproductinfoa) Per il corretto funzionamento di FindRelatedProducts, l'autore del pacchetto deve assicurarsi che la proprietà [**ProductLanguage**](productlanguage.md) sia impostata nella tabella Proprietà su una lingua elencata anche nella proprietà [**Riepilogo**](template-summary.md) modelli.
5.  Se si crea un pacchetto di installazione per la prima versione del prodotto, usare un nuovo [**upgradeCode**](upgradecode.md). Se il pacchetto è destinato a una versione più recente di un prodotto esistente o è la stessa versione di un prodotto esistente in una lingua diversa, usare lo stesso [**codice**](upgradecode.md) di aggiornamento del prodotto esistente. Non due prodotti con lo stesso [**ProductVersion**](productversion.md) e lo stesso [**ProductLanguage**](productlanguage.md) possono avere lo stesso [**UpgradeCode,**](upgradecode.md)a meno che uno non sia un piccolo [aggiornamento](small-updates.md) dell'altro.
6.  [**UpgradeCode**](upgradecode.md) ha il formato di [un GUID](guid.md). Immettere il GUID [**UpgradeCode**](upgradecode.md) nella tabella Proprietà.

Per altre informazioni, vedere [Impedire l'installazione](preventing-an-old-package-from-installing-over-a-newer-version.md)di un pacchetto precedente in una versione più recente.

 

 



