---
title: Denominazione di attributi e classi
description: Questo argomento include le linee guida per la denominazione degli attributi e delle classi.
ms.assetid: ccbc2859-332f-4ded-9125-5bf507cad960
ms.tgt_platform: multiple
keywords:
- Denominazione di attributi e classi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 80bfd2614033e12f68ba2727cc7aec689c16071e
ms.sourcegitcommit: 02e6e0b58720bf6b77797dd7a9ddc11c95f42b33
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/21/2020
ms.locfileid: "106300680"
---
# <a name="naming-attributes-and-classes"></a>Denominazione di attributi e classi

Questo argomento include le linee guida per la denominazione degli attributi e delle classi.

Per creare una nuova classe o attributo, attenersi alle seguenti regole di denominazione:

-   Usare lo stesso nome per le proprietà **CN** e **ldapDisplayName** di un nuovo oggetto **attributeSchema** o **classSchema** .
-   Identificare la società con un prefisso minuscolo nella prima sezione del nome. Questo prefisso può essere un nome DNS, un acronimo o un'altra stringa che identifica in modo univoco l'azienda. Il prefisso garantisce che tutti gli attributi e le classi per una società specifica vengano visualizzati consecutivamente durante l'esplorazione dello schema.
-   Se si sviluppa un'estensione dello schema come fornitore di software indipendente, aggiungere un'abbreviazione del nome del prodotto del prefisso. In questo modo viene aggiunta la distinzione tra più prodotti che contengono estensioni dello schema LDAP.
-   Usare un trattino come carattere successivo dopo il prefisso.
-   Specificare un attributo o un nome di classe univoco all'interno degli attributi della società dopo il segno meno. Questa parte del nome comune deve essere descrittiva. Non usare nomi illogici privi di significato per sviluppatori e visualizzatori dello schema.

Se, ad esempio, la società fittizia Fabrikam ha esteso lo schema aggiungendo un attributo per l'archiviazione di un identificatore della posta vocale, il **CN** e il **ldapDisplayName** del nuovo attributo potrebbero essere "Fabrikam-VoiceMailID".

Se il **ldapDisplayName** di un attributo o di una classe non è specificato, il sistema usa il **CN** per generarne uno. Tuttavia, l'algoritmo di sistema per la generazione del nome può causare conflitti di nomi o nomi difficili da leggere. Per evitare questi problemi, è consigliabile specificare in modo esplicito un **ldapDisplayName** per tutti gli attributi e le classi.

Per finalità di sviluppo e test, potrebbe essere opportuno aggiungere un suffisso di versione a **CN** e **ldapDisplayName**, ad esempio "Fabrikam-VoiceMailID-001". In un ambiente di sviluppo/test distribuito, un suffisso di versione consente agli sviluppatori di eseguire contemporaneamente più versioni del software. Al termine del test, rinominare l'attributo o la classe per rimuovere il suffisso.

Non è possibile eliminare le versioni inattive di un'estensione dello schema, ma è possibile disabilitarle e rinominarle con nomi oscuri. Per ulteriori informazioni, vedere la pagina relativa alla [disabilitazione di classi e attributi esistenti](disabling-existing-classes-and-attributes.md).

 

 




