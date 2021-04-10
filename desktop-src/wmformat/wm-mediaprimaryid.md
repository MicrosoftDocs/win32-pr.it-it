---
title: WM/MediaClassPrimaryID
description: L'attributo WM/MediaClassPrimaryID contiene il GUID della classe multimediale primaria.
ms.assetid: 1d01e273-e6ec-49f1-90af-5c2ae171b199
keywords:
- Formato di Windows Media WM/MediaClassPrimaryID
topic_type:
- apiref
api_name:
- WM/MediaClassPrimaryID
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a8f84d987d57b1d825fac54e6a7de41b0154952e
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/25/2019
ms.locfileid: "103857578"
---
# <a name="wmmediaclassprimaryid"></a>WM/MediaClassPrimaryID

L'attributo **WM/MediaClassPrimaryID** contiene il GUID della classe multimediale primaria.

## <a name="global-constant"></a>Costante globale

g \_ wszWMMediaClassPrimaryID

## <a name="data-type"></a>Tipo di dati

**\_GUID di tipo WMT \_**

## <a name="remarks"></a>Commenti

Questo attributo deve essere impostato su uno dei valori riportati nella tabella seguente.



| GUID della classe primaria                     | Descrizione                                                  |
|----------------------------------------|--------------------------------------------------------------|
| "D1607DBC-E323-4BE2-86A1-48A42A28441E" | Da usare per i file musicali. Non usare per audio che non sia musica. |
| "DB9830BD-3AB3-4FAB-8A37-1A995F7FF74B" | Da usare per i file video.                                         |
| "01CD0F29-DA4E-4157-897B-6275D50C4F11" | Utilizzare per i file audio che non sono musica.                      |
| "FCF24A76-9A57-4036-990D-E35DD8B244E1" | Utilizzare per i file che non sono audio o video.               |



 

Quando si specifica un identificatore di classe primario, è necessario impostare anche un identificatore di classe secondaria per chiarire il tipo di contenuto nel file.

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Elenco degli attributi**](attribute-list.md)
</dt> <dt>

[**WM/MediaClassSecondaryID**](wm-mediasecondaryid.md)
</dt> </dl>

 

 




