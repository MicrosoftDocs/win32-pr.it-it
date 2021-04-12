---
description: La tabella PacchettoPatch descrive tutti i pacchetti di patch applicati al prodotto. Per ogni pacchetto di patch, l'identificatore univoco per la patch viene fornito insieme alle informazioni sull'immagine multimediale in cui si trova la patch.
ms.assetid: 212d99dd-c80c-42ca-9dfa-819ae1813006
title: Tabella PacchettoPatch
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b13bf9fc03012ca54a0b2144e97c828c968c68da
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104234026"
---
# <a name="patchpackage-table"></a>Tabella PacchettoPatch

La tabella PacchettoPatch descrive tutti i pacchetti di patch applicati al prodotto. Per ogni pacchetto di patch, l'identificatore univoco per la patch viene fornito insieme alle informazioni sull'immagine multimediale in cui si trova la patch.

La tabella PacchettoPatch include le colonne seguenti.



| Colonna  | Tipo                   | Chiave | Nullable |
|---------|------------------------|-----|----------|
| PatchId | [GUID](guid.md)       | S   | N        |
| File multimediali\_ | [Integer](integer.md) | N   | N        |



 

## <a name="columns"></a>Colonne

<dl> <dt>

<span id="PatchId"></span><span id="patchid"></span><span id="PATCHID"></span>PatchId
</dt> <dd>

Questa colonna contiene un identificatore univoco per questa patch particolare.

</dd> <dt>

<span id="Media_"></span><span id="media_"></span><span id="MEDIA_"></span>Media\_
</dt> <dd>

Questa colonna è una chiave esterna per la colonna DiskID della [tabella dei supporti](media-table.md) e indica il disco contenente il pacchetto di patch.

</dd> </dl>

## <a name="remarks"></a>Commenti

La tabella PacchettoPatch è obbligatoria in ogni pacchetto di patch. Se la tabella non è presente, i tentativi di installazione della patch avranno esito negativo con l'errore 2768: la trasformazione nel pacchetto della patch non è valida. Questa tabella viene in genere aggiunta al pacchetto di installazione da una trasformazione da un pacchetto di patch. Non viene in genere creato direttamente in un pacchetto di installazione.

## <a name="validation"></a>Convalida

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
</dl>

 

 



