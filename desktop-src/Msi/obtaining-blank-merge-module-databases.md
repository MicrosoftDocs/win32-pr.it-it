---
description: Ottenere un database del modulo unione vuoto. È possibile usare il file Schema.msm fornito con Windows Installer SDK come database iniziale per il modulo di unione. Per altre informazioni, vedere Windows SDK Components for Windows Installer Developers (Componenti SDK per Windows programma di installazione).
ms.assetid: 8408e892-adc6-4ef5-ad36-4d04c021c899
title: Recupero di database di moduli unione vuoti
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 87b5da0a9ad108ab320458934a26b5ec22727d7f11cabee9d870dd7fc01dc84c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118943301"
---
# <a name="obtaining-blank-merge-module-databases"></a>Recupero di database di moduli unione vuoti

Ottenere un database del modulo unione vuoto. È possibile usare il file Schema.msm fornito con Windows Installer SDK come database iniziale per il modulo di unione. Per altre informazioni, vedere Windows [SDK Components for Windows Installer Developers](platform-sdk-components-for-windows-installer-developers.md).

Gli sviluppatori devono creare moduli unione usando lo schema di database più semplice che installa i componenti. L'uso di uno schema semplice garantisce la massima compatibilità per il modulo di merge. L'unione di un modulo unione in un pacchetto di installazione con uno schema di database diverso comporta in genere conflitti di merge.

Per un elenco completo di tutte le tabelle obbligatorie e facoltative nei moduli unione, vedere [Merge Module Database Tables](merge-module-database-tables.md).

 

 



