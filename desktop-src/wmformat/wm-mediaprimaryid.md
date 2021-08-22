---
title: WM/MediaClassPrimaryID
description: L'attributo WM/MediaClassPrimaryID contiene il GUID della classe multimediale primaria.
ms.assetid: 1d01e273-e6ec-49f1-90af-5c2ae171b199
keywords:
- Formato multimediale windows WM/MediaClassPrimaryID
topic_type:
- apiref
api_name:
- WM/MediaClassPrimaryID
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d650c15a861cdf55af07fba6d47fb416d61a56d399b855efc461cddd2f628edf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119027059"
---
# <a name="wmmediaclassprimaryid"></a>WM/MediaClassPrimaryID

**L'attributo WM/MediaClassPrimaryID** contiene il GUID della classe multimediale primaria.

## <a name="global-constant"></a>Costante globale

g \_ wszWMMediaClassPrimaryID

## <a name="data-type"></a>Tipo di dati

**GUID DI TIPO WMT \_ \_**

## <a name="remarks"></a>Commenti

Questo attributo deve essere impostato su uno dei valori nella tabella seguente.



| GUID classe primaria                     | Descrizione                                                  |
|----------------------------------------|--------------------------------------------------------------|
| "D1607DBC-E323-4BE2-86A1-48A42A28441E" | Usare per i file musicali. Non usare per l'audio che non è musica. |
| "DB9830BD-3AB3-4FAB-8A37-1A995F7FF74B" | Usare per i file video.                                         |
| "01CD0F29-DA4E-4157-897B-6275D50C4F11" | Usare per i file audio che non sono musica.                      |
| "FCF24A76-9A57-4036-990D-E35DD8B244E1" | Usare per i file che non sono audio o video.               |



 

Quando si specifica un identificatore di classe primaria, è necessario impostare anche un identificatore di classe secondario per chiarire il tipo di contenuto nel file.

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Elenco degli attributi**](attribute-list.md)
</dt> <dt>

[**WM/MediaClassSecondaryID**](wm-mediasecondaryid.md)
</dt> </dl>

 

 




