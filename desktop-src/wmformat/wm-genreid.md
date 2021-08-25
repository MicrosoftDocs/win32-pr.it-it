---
title: WM/GenreID
description: L'attributo WM/GenreID contiene un identificatore di genere conforme al contenuto del tag TCON in ID3v2.
ms.assetid: 2f2a87f7-ba2d-465a-a36b-a8f58b5dd2d0
keywords:
- WM/GenreID windows Media Format
topic_type:
- apiref
api_name:
- WM/GenreID
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9355a16196d386d4ec3f2a98588eced2981f8e62a3df96a9c0d094551a10a733
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119930441"
---
# <a name="wmgenreid"></a>WM/GenreID

**L'attributo WM/GenreID** contiene un identificatore di genere conforme al contenuto del tag TCON in ID3v2. Deve contenere l'ID genere tra parentesi, seguito facoltativamente da un perfezionamento che descrive ulteriormente il genere. Per altre informazioni, vedere la specifica ID3v2.

## <a name="global-constant"></a>Costante globale

g \_ wszWMGenreID

## <a name="data-type"></a>Tipo di dati

**STRINGA DI \_ TIPO \_ WMT**

## <a name="remarks"></a>Commenti

L'attributo preferito per specificare un genere è [**WM/Genre.**](wm-genre.md) Usarlo in preferenza per questo attributo.

Se si modifica **WM/Genre** o **WM/GenreID** in un file MP3, l'altro attributo verrà modificato in modo che corrisponda.

### <a name="example"></a>Esempio



| Tipo file | Valore di esempio   |
|-----------|-----------------|
| Audio     | "(4) Eurodisco" |



 

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Elenco degli attributi**](attribute-list.md)
</dt> </dl>

 

 




