---
description: La tabella MIME associa un tipo di contenuto MIME con un'estensione di file o un CLSID per generare le informazioni sull'estensione o sul server COM richieste per l'annuncio del contenuto MIME (Multipurpose Internet Mail Extensions).
ms.assetid: 5d452b24-ae04-4c45-8b3b-48e81f13a21e
title: Tabella MIME
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ca11c8596e8f3735872c88668211953fc2b18b52
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104232850"
---
# <a name="mime-table"></a>Tabella MIME

La tabella MIME associa un tipo di contenuto MIME con un'estensione di file o un CLSID per generare le informazioni sull'estensione o sul server COM richieste per l'annuncio del contenuto MIME (Multipurpose Internet Mail Extensions).

La tabella MIME contiene le colonne seguenti.



| Colonna      | Tipo             | Chiave | Nullable |
|-------------|------------------|-----|----------|
| ContentType | [Text](text.md) | S   | N        |
| Estensione\_ | [Text](text.md) | N   | N        |
| CLSID       | [GUID](guid.md) | N   | S        |



 

## <a name="columns"></a>Colonne

<dl> <dt>

<span id="ContentType"></span><span id="contenttype"></span><span id="CONTENTTYPE"></span>ContentType
</dt> <dd>

Questa colonna è un identificatore per il contenuto MIME. Viene in genere scritto in formato tipo/formato.

</dd> <dt>

<span id="Extension_"></span><span id="extension_"></span><span id="EXTENSION_"></span>Estensione\_
</dt> <dd>

Questa colonna contiene l'estensione del server da associare al contenuto MIME, senza il punto. Questa colonna è una chiave esterna nella [tabella di estensione](extension-table.md). La tabella di estensione contiene informazioni sul server di estensione del nome file che vengono utilizzate come parte di un annuncio pubblicitario.

</dd> <dt>

<span id="CLSID"></span><span id="clsid"></span>CLSID
</dt> <dd>

Questa colonna contiene il CLSID del server COM da associare al contenuto MIME. Il CLSID in questa colonna può essere una chiave esterna nella [tabella della classe](class-table.md) oppure può essere un CLSID già esistente nel computer dell'utente. La tabella della classe contiene informazioni relative al server COM utilizzate come parte dell'annuncio.

</dd> </dl>

## <a name="remarks"></a>Commenti

Questa tabella viene definita quando viene eseguita l'azione [RegisterMIMEInfo](registermimeinfo-action.md) o [UnregisterMIMEInfo](unregistermimeinfo-action.md) . In modalità di annuncio, l'azione RegisterMIMEInfo registra tutte le informazioni MIME per i server dalla tabella MIME per cui è abilitata la funzionalità corrispondente. In caso contrario, l'azione registra le informazioni MIME per i server dalla tabella MIME per cui è attualmente selezionata la funzionalità corrispondente da installare. L' [azione UnregisterMIMEInfo](unregistermimeinfo-action.md) Annulla la registrazione delle informazioni del registro di sistema correlate a MIME dal sistema. L'azione annulla la registrazione delle informazioni MIME per i server dalla tabella MIME per cui è attualmente selezionata la funzionalità corrispondente per la disinstallazione.

## <a name="validation"></a>Convalida

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE15](ice15.md)  
[ICE32](ice32.md)  
</dl>

 

 



