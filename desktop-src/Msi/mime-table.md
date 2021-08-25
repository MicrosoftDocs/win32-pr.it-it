---
description: La tabella MIME associa un tipo di contenuto MIME a un'estensione di file o a un CLSID per generare l'estensione o le informazioni sul server COM necessarie per l'annuncio del contenuto MIME (Multipurpose Internet Mail Extensions).
ms.assetid: 5d452b24-ae04-4c45-8b3b-48e81f13a21e
title: Tabella MIME
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a9e8a8f83499e286b63bf24dffa8858329231e74eec1f641588230da51578007
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119913371"
---
# <a name="mime-table"></a>Tabella MIME

La tabella MIME associa un tipo di contenuto MIME a un'estensione di file o a un CLSID per generare l'estensione o le informazioni sul server COM necessarie per l'annuncio del contenuto MIME (Multipurpose Internet Mail Extensions).

La tabella MIME include le colonne seguenti.



| Colonna      | Tipo             | Chiave | Nullable |
|-------------|------------------|-----|----------|
| ContentType | [Text](text.md) | S   | N        |
| Estensione\_ | [Text](text.md) | N   | N        |
| CLSID       | [GUID](guid.md) | N   | S        |



 

## <a name="columns"></a>Colonne

<dl> <dt>

<span id="ContentType"></span><span id="contenttype"></span><span id="CONTENTTYPE"></span>Contenttype
</dt> <dd>

Questa colonna è un identificatore per il contenuto MIME. In genere è scritto sotto forma di tipo/formato.

</dd> <dt>

<span id="Extension_"></span><span id="extension_"></span><span id="EXTENSION_"></span>Estensione\_
</dt> <dd>

Questa colonna contiene l'estensione del server che deve essere associata al contenuto MIME, senza il punto. Questa colonna è una chiave esterna nella tabella [extension](extension-table.md). La tabella Extension contiene informazioni sul server dell'estensione di file che vengono usate come parte dell'annuncio.

</dd> <dt>

<span id="CLSID"></span><span id="clsid"></span>Clsid
</dt> <dd>

Questa colonna contiene il CLSID del server COM da associare al contenuto MIME. Il CLSID in questa colonna può essere una chiave esterna nella tabella [Class](class-table.md) o un CLSID già esistente nel computer dell'utente. La tabella Class contiene informazioni correlate al server COM che vengono usate come parte dell'annuncio pubblicitario.

</dd> </dl>

## <a name="remarks"></a>Commenti

Questa tabella viene indicata quando viene eseguita [l'azione RegisterMIMEInfo](registermimeinfo-action.md) o [UnregisterMIMEInfo.](unregistermimeinfo-action.md) In modalità di annuncio, l'azione RegisterMIMEInfo registra tutte le informazioni MIME per i server dalla tabella MIME per cui è abilitata la funzionalità corrispondente. In caso contrario, l'azione registra le informazioni MIME per i server della tabella MIME per cui è attualmente selezionata l'installazione della funzionalità corrispondente. [L'azione UnregisterMIMEInfo](unregistermimeinfo-action.md) annulla la registrazione delle informazioni del Registro di sistema relative a MIME dal sistema. L'azione annulla la registrazione delle informazioni MIME per i server della tabella MIME per cui la funzionalità corrispondente è attualmente selezionata per la disinstallazione.

## <a name="validation"></a>Convalida

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE15](ice15.md)  
[ICE32](ice32.md)  
</dl>

 

 



