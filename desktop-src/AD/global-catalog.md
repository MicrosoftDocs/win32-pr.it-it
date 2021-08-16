---
title: Catalogo globale
description: Un dominio eseguito da Active Directory Domain Services può essere costituito da più partizioni o contesti di denominazione.
ms.assetid: eac02c1f-0c37-4eee-822d-07913ea8775a
ms.tgt_platform: multiple
keywords:
- Active Directory del catalogo globale
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e81abf04ab3e4d95819f91b5db8753a265e49ca79b2f405a32665dc46a8f2db5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118189116"
---
# <a name="global-catalog"></a>Catalogo globale

Un dominio eseguito da Active Directory Domain Services può essere costituito da più partizioni o contesti di denominazione. Il nome distinto (DN) di un oggetto include informazioni sufficienti per individuare una replica della partizione che contiene l'oggetto. Spesso, tuttavia, l'utente o l'applicazione non conosce il DN dell'oggetto di destinazione o quale partizione potrebbe contenere l'oggetto. Il [*catalogo globale (GC) consente*](/previous-versions/windows/desktop/legacy/ms681905(v=vs.85)) a utenti e applicazioni di trovare oggetti in un albero di dominio di Active Directory, dati uno o più attributi dell'oggetto di destinazione.

Il catalogo globale contiene una replica parziale di ogni contesto dei nomi nella directory. Contiene anche i contesti di denominazione dello schema e della configurazione. Ciò significa che il Garbage Collector contiene una replica di ogni oggetto nella directory, ma con solo un numero ridotto di attributi. Gli attributi nel Garbage Collector sono quelli usati più di frequente nelle operazioni di ricerca (ad esempio nome e cognome o nomi di accesso di un utente) e quelli necessari per individuare una replica completa dell'oggetto. Il catalogo globale consente agli utenti di trovare rapidamente gli oggetti di interesse senza sapere quale dominio li contiene e senza richiedere uno spazio dei nomi esteso contiguo nell'organizzazione.

Il catalogo globale viene compilato automaticamente dal Active Directory Domain Services di replica. La topologia di replica per il catalogo globale viene generata automaticamente. Le proprietà replicate nel catalogo globale includono un set di base definito da Microsoft. Gli amministratori possono specificare proprietà aggiuntive per soddisfare le esigenze di installazione.

 

 