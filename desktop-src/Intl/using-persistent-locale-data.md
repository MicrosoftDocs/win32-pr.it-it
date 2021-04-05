---
description: Utilizzo di dati locali persistenti
ms.assetid: f62402d6-31de-4ff7-9538-7925a007a089
title: Utilizzo di dati locali persistenti
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b4fe4990da53e4db9f71b2feffbd9eb40aedee9e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103885721"
---
# <a name="using-persistent-locale-data"></a>Utilizzo di dati locali persistenti

Un'applicazione globalizzata spesso rende permanente o trasmette dati, ad esempio data e ora. Quando si decide in che modo l'applicazione deve gestire la persistenza dei dati, tenere presente che i dati non sono necessariamente uguali da computer a computer o da esecuzioni dell'applicazione. Questo vale sia per le [impostazioni locali](locales-and-languages.md) fornite con le [impostazioni locali](custom-locales.md)di Windows che per quelle personalizzate.

La progettazione dell'applicazione deve prendere in considerazione una serie di modifiche ai dati correlate alle impostazioni locali che possono verificarsi. Ad esempio:

-   I simboli di valuta possono cambiare quando i paesi adottano l'euro.
-   Le preferenze internazionali possono cambiare. Ad esempio, il formato d/m/y potrebbe variare nel formato m/d/y per determinate impostazioni locali.
-   L'ortografia dei nomi dei giorni può variare a causa delle riforme ortografiche. Inoltre, la combinazione di maiuscole e minuscole può variare per i nomi dei mesi

## <a name="use-locale-independent-formats-for-storage-and-data-interchange"></a>Usare formati di Locale-Independent per l'archiviazione e l'interscambio dati

Un'applicazione che rende permanente i dati deve usare formati indipendenti dalle impostazioni locali per l'archiviazione e l'interscambio dati. Esempi sono formati hardcoded o standard; le impostazioni locali invariabili del [ \_ nome delle \_ Impostazioni](locale-name-constants.md)locali e dei formati di archiviazione binari.

Se sono necessari dati di ordinamento permanenti, l'applicazione deve utilizzare la funzione [**CompareStringOrdinal**](/windows/desktop/api/Stringapiset/nf-stringapiset-comparestringordinal) . Tenere presente che un formato invariante non rimane invariante per l' [ordinamento](sorting.md), solo per le impostazioni locali e i dati del calendario.

## <a name="use-the-user-default-locale-for-data-presentation"></a>Usare le impostazioni locali predefinite dell'utente per la presentazione dei dati

Per presentare i dati persistenti, è preferibile che l'applicazione riformatta i dati utilizzando le impostazioni locali predefinite dell'utente. L'utilizzo di queste impostazioni locali consente l'override degli utenti. Per ulteriori informazioni, vedere [impostazioni locali \_ dell' \_ utente](locale-user-default.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Uso del supporto per le lingue nazionali](using-national-language-support.md)
</dt> <dt>

[Impostazioni locali personalizzate](custom-locales.md)
</dt> <dt>

[Ordinamento](sorting.md)
</dt> </dl>

 

 



