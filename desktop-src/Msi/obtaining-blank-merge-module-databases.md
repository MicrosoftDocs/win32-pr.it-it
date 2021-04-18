---
description: Ottenere un database del modulo merge vuoto. È possibile usare il file schema. msm fornito con Windows Installer SDK come database iniziale per il modulo merge. Per ulteriori informazioni, vedere Windows SDK Components for Windows Installer Developers.
ms.assetid: 8408e892-adc6-4ef5-ad36-4d04c021c899
title: Recupero di database del modulo merge vuoti
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2ba75d55763d30b0ab545d2dbddbc19c1b0c279d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106309993"
---
# <a name="obtaining-blank-merge-module-databases"></a>Recupero di database del modulo merge vuoti

Ottenere un database del modulo merge vuoto. È possibile usare il file schema. msm fornito con Windows Installer SDK come database iniziale per il modulo merge. Per ulteriori informazioni, vedere [Windows SDK Components for Windows Installer Developers](platform-sdk-components-for-windows-installer-developers.md).

Gli sviluppatori devono creare moduli unione usando lo schema di database più semplice che installa i componenti. L'utilizzo di uno schema semplice garantisce la massima compatibilità per il modulo merge. L'Unione di un modulo merge in un pacchetto di installazione con uno schema di database diverso in genere comporta conflitti di merge.

Per un elenco completo di tutte le tabelle obbligatorie e facoltative nei moduli merge, vedere [Merge Module Database Tables](merge-module-database-tables.md).

 

 



