---
title: WM/GenreID
description: L'attributo WM/GenreID contiene un identificatore di genere conforme al contenuto del tag TCON in ID3v2.
ms.assetid: 2f2a87f7-ba2d-465a-a36b-a8f58b5dd2d0
keywords:
- Formato di Windows Media WM/GenreID
topic_type:
- apiref
api_name:
- WM/GenreID
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0a3b25dffe69471f47eaf20124af48141835540f
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/25/2019
ms.locfileid: "104398044"
---
# <a name="wmgenreid"></a>WM/GenreID

L'attributo **WM/GenreID** contiene un identificatore di genere conforme al contenuto del tag TCON in id3v2. Questo deve contenere l'ID del genere tra parentesi, seguito facoltativamente da un perfezionamento che descrive ulteriormente il genere. Per ulteriori informazioni, vedere la specifica ID3v2.

## <a name="global-constant"></a>Costante globale

g \_ wszWMGenreID

## <a name="data-type"></a>Tipo di dati

**\_stringa di tipo WMT \_**

## <a name="remarks"></a>Commenti

L'attributo preferito per specificare un genere è [**WM/genre**](wm-genre.md). Utilizzare questo attributo in modo preferenziale.

Se si modifica **WM/genre** o **WM/GenreID** in un file MP3, l'altro attributo verrà modificato in modo che corrisponda a.

### <a name="example"></a>Esempio



| Tipo file | Valore di esempio   |
|-----------|-----------------|
| Audio     | "(4) Eurodisco" |



 

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Elenco degli attributi**](attribute-list.md)
</dt> </dl>

 

 




