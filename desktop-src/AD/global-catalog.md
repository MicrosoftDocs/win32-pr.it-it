---
title: Catalogo globale
description: Un dominio eseguito da Active Directory Domain Services può essere costituito da numerose partizioni o contesti di denominazione.
ms.assetid: eac02c1f-0c37-4eee-822d-07913ea8775a
ms.tgt_platform: multiple
keywords:
- catalogo globale Active Directory
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b4496804d21e53cf2d87947288179e7f96ca75c8
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/17/2020
ms.locfileid: "103724511"
---
# <a name="global-catalog"></a>Catalogo globale

Un dominio eseguito da Active Directory Domain Services può essere costituito da numerose partizioni o contesti di denominazione. Il nome distinto (DN) di un oggetto include informazioni sufficienti per individuare una replica della partizione che contiene l'oggetto. In molti casi, tuttavia, l'utente o l'applicazione non conosce il DN dell'oggetto di destinazione o quale partizione potrebbe contenere l'oggetto. Il [*catalogo globale (GC)*](/previous-versions/windows/desktop/legacy/ms681905(v=vs.85)) consente a utenti e applicazioni di trovare oggetti in un albero Active Directory dominio, in base a uno o più attributi dell'oggetto di destinazione.

Il catalogo globale contiene una replica parziale di ogni contesto di denominazione presente nella directory. Contiene anche i contesti di denominazione dello schema e della configurazione. Ciò significa che il GC include una replica di ogni oggetto nella directory, ma con un numero ridotto di attributi. Gli attributi nel GC sono quelli usati più di frequente nelle operazioni di ricerca, ad esempio il nome e il cognome di un utente o i nomi di accesso, e quelli necessari per individuare una replica completa dell'oggetto. Il GC consente agli utenti di trovare rapidamente oggetti di interesse senza sapere quale dominio li contiene e senza richiedere uno spazio dei nomi esteso contiguo nell'azienda.

Il catalogo globale viene compilato automaticamente dal sistema di replica Active Directory Domain Services. La topologia di replica per il catalogo globale viene generata automaticamente. Le proprietà replicate nel catalogo globale includono un set di base definito da Microsoft. Gli amministratori possono specificare proprietà aggiuntive per soddisfare le esigenze di installazione.

 

 