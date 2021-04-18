---
description: Questo argomento non è aggiornato. Per informazioni aggiornate, vedere la specifica dello schema di stampa.
ms.assetid: ff966475-626d-4a48-9349-e60454d47c57
title: Parole chiave pubbliche dello schema di stampa
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8e3e8fb9a46bbed2b135f4e81456dd65e79be830
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/05/2021
ms.locfileid: "106321014"
---
# <a name="print-schema-public-keywords"></a>Parole chiave pubbliche dello schema di stampa

Questo argomento non è aggiornato. Per informazioni aggiornate, vedere la [specifica dello schema di stampa](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

Nella sezione seguente vengono specificate le parole chiave pubbliche definite per lo schema di stampa.

## <a name="print-schema-public-keywords-usage-for-print-capabilities"></a>Utilizzo delle parole chiave pubbliche dello schema di stampa per le funzionalità di stampa

Le parole chiave specificate nelle parole chiave Public PrintCapabilities possono essere visualizzate in un documento sulle funzionalità di stampa. Per ulteriori informazioni sul modo in cui queste parole chiave interagiscono con la tecnologia PrintCapabilities, vedere [Cenni preliminari](overview-of-the-printcapabilities.md) sulla sezione PrintCapabilities.

Le parole chiave pubbliche specifiche per PrintTicket non devono essere visualizzate in un documento PrintCapabilities.

## <a name="print-schema-public-keywords-usage-for-printticket"></a>Utilizzo delle parole chiave pubbliche dello schema di stampa per PrintTicket

Le parole chiave specificate in PrintTicket Public Keywords possono essere visualizzate in un oggetto PrintTicket. Le parole chiave PrintTicket vengono implementate come tipo di elemento Property. Per ulteriori informazioni sul modo in cui queste parole chiave interagiscono con la tecnologia PrintTicket, vedere la sezione [informazioni di configurazione non correlate a PrintCapabilities](configuration-information-not-related-to-printcapabilities.md) .

Le parole chiave specificate in PrintCapabilities Public Keywords possono essere visualizzate in un oggetto PrintTicket a seconda dell'implementazione di PrintTicket in un'applicazione e/o in un driver. In questo modo vengono fornite le selezioni per gli attributi del dispositivo definiti nel documento PrintCapabilities. Per ulteriori informazioni sull'interazione tra le parole chiave PrintCapabilities e l'oggetto PrintTicket, consultare lo [scopo della sezione PrintTicket](purpose-of-the-printticket.md) .

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Specifica dello schema di stampa](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



