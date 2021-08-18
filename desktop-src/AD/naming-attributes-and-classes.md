---
title: Denominazione di attributi e classi
description: Questo argomento include linee guida per la denominazione di attributi e classi.
ms.assetid: ccbc2859-332f-4ded-9125-5bf507cad960
ms.tgt_platform: multiple
keywords:
- Denominazione di attributi e classi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e042decaf7d3dd15606ea7e138d9e6315d4200f2a641c10381951f2657a5aafe
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118186001"
---
# <a name="naming-attributes-and-classes"></a>Denominazione di attributi e classi

Questo argomento include linee guida per la denominazione di attributi e classi.

Per creare una nuova classe o attributo, attenersi alle regole di denominazione seguenti:

-   Usare lo stesso nome per le proprietà **cn** e **lDAPDisplayName** di un nuovo **oggetto attributeSchema** **o classSchema.**
-   Identificare la società con un prefisso minuscolo nella prima sezione del nome. Questo prefisso può essere un nome DNS, un acronimo o un'altra stringa che identifica in modo univoco la società. Il prefisso garantisce che tutti gli attributi e le classi per una società specifica siano visualizzati consecutivamente durante l'esplorazione dello schema.
-   Se si sviluppa un'estensione dello schema come fornitore di software indipendente, aggiungere un'abbreviazione del nome del prodotto del prefisso. Ciò aggiunge la distinzione tra più prodotti che contengono estensioni dello schema LDAP.
-   Usare un trattino come carattere successivo dopo il prefisso.
-   Specificare un attributo o un nome di classe univoco all'interno degli attributi della società dopo il trattino. Questa parte del nome comune deve essere descrittiva. Non usare nomi illogici che non hanno significato per sviluppatori e visualizzatori dello schema.

Ad esempio, se la società Fittizia Fabrikam ha esteso lo schema aggiungendo un attributo per l'archiviazione di un identificatore di casella vocale, **cn** e **lDAPDisplayName** del nuovo attributo potrebbero essere "fabrikam-VoiceMailID".

Se **lDAPDisplayName di** un attributo o di una classe non è specificato, il sistema usa **cn** per generarne uno. Tuttavia, l'algoritmo di sistema per la generazione del nome può causare conflitti di nomi o nomi difficili da leggere. Per evitare questi problemi, è consigliabile specificare in modo esplicito **lDAPDisplayName** per tutti gli attributi e le classi.

A scopo di sviluppo e test, può essere opportuno aggiungere un suffisso di versione a **cn** e **lDAPDisplayName,** ad esempio "fabrikam-VoiceMailID-001". In un ambiente di sviluppo/test distribuito, un suffisso di versione consente agli sviluppatori di eseguire più versioni del software contemporaneamente. Al termine del test, rinominare l'attributo o la classe per rimuovere il suffisso.

Non è possibile eliminare le versioni inattive di estensioni dello schema, ma è possibile disabilitarle e rinominarle con nomi sconosciuti. Per altre informazioni, vedere [Disabilitazione di classi e attributi esistenti.](disabling-existing-classes-and-attributes.md)

 

 




