---
description: La tabella PatchPackage descrive tutti i pacchetti di patch applicati a questo prodotto. Per ogni pacchetto di patch, viene fornito l'identificatore univoco della patch insieme alle informazioni sull'immagine del supporto in cui si trova la patch.
ms.assetid: 212d99dd-c80c-42ca-9dfa-819ae1813006
title: Tabella PatchPackage
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: da4027913854436072330a69a788ca9dc9b1365a71b82fd1727227e33d8a203b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119926121"
---
# <a name="patchpackage-table"></a>Tabella PatchPackage

La tabella PatchPackage descrive tutti i pacchetti di patch applicati a questo prodotto. Per ogni pacchetto di patch, viene fornito l'identificatore univoco della patch insieme alle informazioni sull'immagine del supporto in cui si trova la patch.

La tabella PatchPackage contiene le colonne seguenti.



| Colonna  | Tipo                   | Chiave | Nullable |
|---------|------------------------|-----|----------|
| PatchId | [GUID](guid.md)       | S   | N        |
| File multimediali\_ | [Integer](integer.md) | N   | N        |



 

## <a name="columns"></a>Colonne

<dl> <dt>

<span id="PatchId"></span><span id="patchid"></span><span id="PATCHID"></span>PatchId
</dt> <dd>

Questa colonna contiene un identificatore univoco per questa particolare patch.

</dd> <dt>

<span id="Media_"></span><span id="media_"></span><span id="MEDIA_"></span>Media\_
</dt> <dd>

Questa colonna è una chiave esterna per la colonna DiskId della [tabella](media-table.md) supporti e indica il disco contenente il pacchetto di patch.

</dd> </dl>

## <a name="remarks"></a>Commenti

La tabella PatchPackage è necessaria in ogni pacchetto di patch. Se la tabella non è presente, i tentativi di installazione della patch hanno esito negativo e viene visualizzato l'errore "Errore 2768: La trasformazione nel pacchetto di patch non è valida". Questa tabella viene in genere aggiunta al pacchetto di installazione da una trasformazione da un pacchetto patch. In genere non viene creato direttamente in un pacchetto di installazione.

## <a name="validation"></a>Convalida

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
</dl>

 

 



