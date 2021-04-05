---
title: Schema (AD DS)
description: Active Directory schema viene implementato come un set di istanze della classe di oggetti archiviate nella directory.
ms.assetid: 77c297ca-0dfc-4545-9832-4202e066822b
ms.tgt_platform: multiple
keywords:
- Active Directory schema Active Directory
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7965232dd756272eb016ca251aa29716a22a088a
ms.sourcegitcommit: 8ea1a82717bd3dbb3457be0697329aa37fb13f08
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/11/2019
ms.locfileid: "103719885"
---
# <a name="schema-ad-ds"></a>Schema (AD DS)

Active Directory schema viene implementato come un set di istanze della classe di oggetti archiviate nella directory. Si tratta di un comportamento molto diverso rispetto a quello di molte directory che dispongono di uno schema, che però viene archiviato come file di testo letto all'avvio. L'archiviazione dello schema nella directory presenta molti vantaggi. Ad esempio, le applicazioni utente possono leggerlo per individuare gli oggetti e le proprietà disponibili.

Active Directory schema può essere aggiornato dinamicamente. Ovvero, un'applicazione può estendere lo schema con nuovi attributi e classi e utilizzare immediatamente le estensioni. Gli aggiornamenti dello schema vengono eseguiti creando o modificando gli oggetti dello schema archiviati nella directory. Analogamente a ogni oggetto in Active Directory, gli elenchi di controllo di accesso (ACL) proteggono gli oggetti dello schema, quindi gli utenti autorizzati possono solo modificare lo schema.

Per ulteriori informazioni, vedere [Active Directory schema](active-directory-schema.md).

 

 




