---
title: Oggetti COM e archiviazione strutturata
description: Uno degli usi correnti più comuni delle proprietà permanenti consiste nell'usarli per archiviare i dati relativi a un oggetto di sistema, ad esempio un documento, con tale oggetto.
ms.assetid: 95136e9a-4c80-4704-ae65-9759487cf8f8
keywords:
- Oggetti COM e archiviazione strutturata
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 472a3d2fb9c145538bbd6b5e87dfcc9523feff78
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104395447"
---
# <a name="com-objects-and-structured-storage"></a>Oggetti COM e archiviazione strutturata

Uno degli usi correnti più comuni delle proprietà permanenti consiste nell'usarli per archiviare i dati relativi a un oggetto di sistema, ad esempio un documento, con tale oggetto. Naturalmente, è possibile archiviare le proprietà con qualsiasi oggetto, ad esempio una stampante, in modo che sia necessario esaminarne solo le proprietà per determinarne la posizione, il tipo e così via. Un oggetto utente può avere un set di proprietà che include dati quali nome, cognome, ufficio e telefono. È possibile scrivere le applicazioni per eseguire una query su un set di oggetti a livello di sistema in base alle relative proprietà, ad esempio per visualizzare tutte le stampanti situate in un determinato edificio. I sistemi correnti, tuttavia, usano più spesso le proprietà sui documenti.

Il set di proprietà primario standard definito da COM è [il set di proprietà informazioni di riepilogo](the-summary-information-property-set.md). Questo set di proprietà è sia semplice che comunemente usato. La maggior parte dei documenti creati dalle applicazioni dispone di un set di attributi comune utile per gli utenti di tali documenti. Questi attributi includono il nome dell'autore del documento, l'oggetto del documento, il momento in cui è stato creato e così via. Sono definiti altri due set di proprietà per Microsoft Office 95, Office 97 e versioni successive. Si tratta del set di proprietà di riepilogo dei documenti COM e del set di proprietà User-Defined proprietà. Per altre informazioni, vedere [formato di set di proprietà serializzato di archiviazione strutturato](structured-storage-serialized-property-set-format.md).

In Windows 3,1 ogni applicazione disponeva di un modo diverso per archiviare questi dati all'interno dei documenti. Per esaminare le informazioni di riepilogo per un determinato documento, l'utente deve eseguire l'applicazione che ha creato il documento, aprirla e richiamare la finestra di dialogo informazioni di riepilogo applicazione, in modo che solo l'applicazione possa visualizzare le informazioni di riepilogo.

I set di proprietà COM e le interfacce dei set di proprietà consentono di visualizzare le proprietà del documento senza eseguire l'applicazione di creazione. Ad esempio, tutte le versioni di Microsoft Word 6,0 o versioni successive e molte altre applicazioni abilitate per COM ora salvano i documenti usando l'archiviazione strutturata COM e il set di proprietà standard descritto qui. Quindi, altre applicazioni di Office Suite sono in grado di visualizzare [il set di proprietà informazioni di riepilogo](the-summary-information-property-set.md) per tale file, purché tale file sia un file di archiviazione strutturata com e l'applicazione di creazione abbia salvato le informazioni nel formato del set di proprietà com. La shell di Windows 95 o Windows 98, ad esempio, usa questo e consente all'utente finale di visualizzare le proprietà di qualsiasi documento di Word 6,0 o versione successiva direttamente dalla Shell.

Per utilizzare i set di proprietà di altre applicazioni, è necessario che le altre applicazioni riconoscano come interpretare le proprietà all'interno di un set di proprietà, che implica uno standard. COM ha sperimentato questo approccio definendo un set di proprietà standard, il set di proprietà informazioni di riepilogo COM. Qualsiasi applicazione con la definizione di questo set di proprietà può accedere facilmente alle informazioni di riepilogo contenute in qualsiasi documento creato da un'applicazione COM che utilizza tale specifica del set di proprietà.

 

 




