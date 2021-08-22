---
title: Oggetti COM e oggetti Archiviazione
description: Uno degli utilizzi correnti più comuni delle proprietà persistenti è l'uso di tali proprietà per archiviare i dati relativi a un oggetto di sistema, ad esempio un documento, con tale oggetto.
ms.assetid: 95136e9a-4c80-4704-ae65-9759487cf8f8
keywords:
- Oggetti COM e oggetti Archiviazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5f4c1405ddfaa060aa249090fc58b25b294a8c9aecc5f7b885d21b55bc162198
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119663591"
---
# <a name="com-objects-and-structured-storage"></a>Oggetti COM e oggetti Archiviazione

Uno degli utilizzi correnti più comuni delle proprietà persistenti è l'uso di tali proprietà per archiviare i dati relativi a un oggetto di sistema, ad esempio un documento, con tale oggetto. Naturalmente esiste il rischio di archiviare le proprietà con qualsiasi oggetto, ad esempio una stampante, quindi sarebbe necessario solo esaminare le relative proprietà per determinarne la posizione, il tipo e così via. Un oggetto utente può avere un set di proprietà che include dati quali nome, cognome, Office e Telefono. Le applicazioni possono essere scritte per eseguire query su un set di oggetti a livello di sistema in base alle relative proprietà, ad esempio visualizzando tutte le stampanti che si trovano in un determinato edificio. I sistemi correnti, tuttavia, usano con maggiore frequenza le proprietà nei documenti.

Lo standard del set di proprietà primario definito da COM è [Il set di proprietà Informazioni di riepilogo](the-summary-information-property-set.md). Questo set di proprietà è semplice e di uso comune. La maggior parte dei documenti creati dalle applicazioni dispone di un set comune di attributi utili per gli utenti di tali documenti. Questi attributi includono il nome dell'autore del documento, l'oggetto del documento, la data di creazione e così via. Altri due set di proprietà sono definiti per Microsoft Office 95, Office 97 e versioni successive. Si tratta del set di proprietà Riepilogo documento COM e del set User-Defined proprietà. Per altre informazioni, vedere [Structured Archiviazione Serialized Property Set Format](structured-storage-serialized-property-set-format.md).

In Windows 3.1, ogni applicazione aveva un modo diverso di archiviare questi dati all'interno dei documenti. Per esaminare le informazioni di riepilogo per un determinato documento, l'utente deve eseguire l'applicazione che ha creato il documento, aprirlo e richiamare la finestra di dialogo Informazioni di riepilogo dell'applicazione, in modo che solo l'applicazione possa visualizzare le informazioni di riepilogo.

I set di proprietà COM e le interfacce dei set di proprietà rendono possibile visualizzare le proprietà del documento senza eseguire l'applicazione di creazione. Ad esempio, tutte le versioni di Microsoft Word 6.0 o versioni successive e molte altre applicazioni abilitate per COM ora salvano i documenti usando l'archiviazione strutturata COM e lo standard del set di proprietà descritto qui. Pertanto, altre applicazioni Office Suite sono [](the-summary-information-property-set.md) in grado di visualizzare il set di proprietà Informazioni di riepilogo per un file di questo tipo, purché tale file sia un file di archiviazione strutturata COM e che l'applicazione di creazione ha salvato le informazioni nel formato set di proprietà COM. La shell Windows 95 o Windows 98, ad esempio, lo usa e consente all'utente finale di visualizzare le proprietà di qualsiasi documento di Word 6.0 o versione successiva direttamente dalla shell.

Per usare i set di proprietà di altre applicazioni, le altre applicazioni devono riconoscere come interpretare le proprietà all'interno di un set di proprietà, che implica uno standard. COM ha integrato questo approccio definendo un set di proprietà standard, il set di proprietà Delle informazioni di riepilogo COM. Qualsiasi applicazione con la definizione di questa proprietà impostata può accedere facilmente alle informazioni di riepilogo contenute in qualsiasi documento creato da un'applicazione COM che usa tale specifica del set di proprietà.

 

 




