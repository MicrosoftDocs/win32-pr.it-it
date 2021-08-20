---
title: Costanti PICTYPE (OleCtl.h)
description: Descrivere il tipo di un oggetto immagine restituito da IPicture get Type, nonché il tipo di immagine nel membro picType della struttura PICTDESC passato a \_ OleCreatePictureIndirect.
ms.assetid: 79f10687-f0eb-4b5e-a1a9-9186dbd0b51f
topic_type:
- apiref
api_name:
- PICTYPE_UNINITIALIZED
- PICTYPE_NONE
- PICTYPE_BITMAP
- PICTYPE_METAFILE
- PICTYPE_ICON
- PICTYPE_ENHMETAFILE
api_location:
- OleCtl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fa6ac7be72ba34616a1ae8d596efbad3af761760c8f5e5c2bfa5dc8362593748
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119567651"
---
# <a name="pictype-constants"></a>Costanti PICTYPE

Descrivere il tipo di un oggetto immagine restituito da [**IPicture::get \_ Type**](/windows/desktop/api/OCIdl/nf-ocidl-ipicture-get_type), nonché il tipo di immagine nel membro **picType** della struttura [**PICTDESC**](/windows/win32/api/olectl/ns-olectl-pictdesc) passato a [**OleCreatePictureIndirect.**](/windows/desktop/api/OleCtl/nf-olectl-olecreatepictureindirect)



| Costante/valore                                                                                                                                                                                                                                  | Descrizione                                                                                                                                                                                                                   |
|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="PICTYPE_UNINITIALIZED"></span><span id="pictype_uninitialized"></span><dl> <dt>**PICTYPE \_ UNINITIALIZED**</dt> <dt>(-1)</dt> </dl> | L'oggetto immagine non è attualmente inizializzato. Questo valore è valido solo come valore restituito dal [**tipo IPicture::get \_**](/windows/desktop/api/OCIdl/nf-ocidl-ipicture-get_type) e non è valido con la [**struttura PICTDESC.**](/windows/win32/api/olectl/ns-olectl-pictdesc)<br/>  |
| <span id="PICTYPE_NONE"></span><span id="pictype_none"></span><dl> <dt>**PICTYPE \_ NONE**</dt> <dt>0</dt> </dl>                               | Un nuovo oggetto immagine deve essere creato senza uno stato inizializzato. Questo valore è valido solo nella [**struttura PICTDESC.**](/windows/win32/api/olectl/ns-olectl-pictdesc)<br/>                                                                        |
| <span id="PICTYPE_BITMAP"></span><span id="pictype_bitmap"></span><dl> <dt>**PICTYPE \_ BITMAP**</dt> <dt>1</dt> </dl>                         | Il tipo di immagine è una bitmap. Quando questo valore si verifica nella [**struttura PICTDESC,**](/windows/win32/api/olectl/ns-olectl-pictdesc) significa che il campo **bmp** di tale struttura contiene i parametri di inizializzazione pertinenti.<br/>             |
| <span id="PICTYPE_METAFILE"></span><span id="pictype_metafile"></span><dl> <dt>**PICTYPE \_ METAFILE**</dt> <dt>2</dt> </dl>                   | Il tipo di immagine è un metafile. Quando questo valore si verifica nella [**struttura PICTDESC,**](/windows/win32/api/olectl/ns-olectl-pictdesc) significa che il campo **wmf** di tale struttura contiene i parametri di inizializzazione pertinenti.<br/>           |
| <span id="PICTYPE_ICON"></span><span id="pictype_icon"></span><dl> <dt>**PICTYPE \_ ICONA**</dt> <dt>3</dt> </dl>                               | Il tipo di immagine è un'icona. Quando questo valore si verifica nella [**struttura PICTDESC,**](/windows/win32/api/olectl/ns-olectl-pictdesc) significa che il campo icona di tale struttura contiene i parametri di inizializzazione pertinenti. <br/>             |
| <span id="PICTYPE_ENHMETAFILE"></span><span id="pictype_enhmetafile"></span><dl> <dt>**PICTYPE \_ ENHMETAFILE**</dt> <dt>4</dt> </dl>          | Il tipo di immagine è un metafile avanzato. Quando questo valore si verifica nella [**struttura PICTDESC,**](/windows/win32/api/olectl/ns-olectl-pictdesc) significa che il campo **emf** di tale struttura contiene i parametri di inizializzazione pertinenti.<br/> |



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                          |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                |
| Intestazione<br/>                   | <dl> <dt>OleCtl.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Tipo IPicture::get \_**](/windows/desktop/api/OCIdl/nf-ocidl-ipicture-get_type)
</dt> <dt>

[**OleCreatePictureIndirect**](/windows/desktop/api/OleCtl/nf-olectl-olecreatepictureindirect)
</dt> <dt>

[**PICTDESC**](/windows/win32/api/olectl/ns-olectl-pictdesc)
</dt> </dl>

 

 





