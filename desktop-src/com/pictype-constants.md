---
title: Costanti PICTYPE (OleCtl. h)
description: Descrive il tipo di un oggetto Picture come restituito da IPicture Get \_ Type, nonché per descrivere il tipo di immagine nel membro picType della struttura PICTDESC che viene passata a OleCreatePictureIndirect.
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
ms.openlocfilehash: bebf8ad8f678e9b6e463ade9f149b2e1d4bab529
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301282"
---
# <a name="pictype-constants"></a>Costanti PICTYPE

Descrive il tipo di un oggetto Picture come restituito da [**IPicture:: Get \_ Type**](/windows/desktop/api/OCIdl/nf-ocidl-ipicture-get_type)e per descrivere il tipo di immagine nel membro **picType** della struttura [**PICTDESC**](/windows/win32/api/olectl/ns-olectl-pictdesc) che viene passata a [**OleCreatePictureIndirect**](/windows/desktop/api/OleCtl/nf-olectl-olecreatepictureindirect).



| Costante/valore                                                                                                                                                                                                                                  | Descrizione                                                                                                                                                                                                                   |
|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="PICTYPE_UNINITIALIZED"></span><span id="pictype_uninitialized"></span><dl> <dt>**PICTYPE \_ Non INIZIALIZZAto**</dt> <dt>(-1)</dt> </dl> | Oggetto immagine attualmente non inizializzato. Questo valore è valido solo come valore restituito da [**IPicture:: Get \_ Type**](/windows/desktop/api/OCIdl/nf-ocidl-ipicture-get_type) e non è valido con la struttura [**PICTDESC**](/windows/win32/api/olectl/ns-olectl-pictdesc) .<br/>  |
| <span id="PICTYPE_NONE"></span><span id="pictype_none"></span><dl> <dt>**PICTYPE \_ NESSUNO**</dt> <dt>0</dt> </dl>                               | Un nuovo oggetto Picture deve essere creato senza uno stato inizializzato. Questo valore è valido solo nella struttura [**PICTDESC**](/windows/win32/api/olectl/ns-olectl-pictdesc) .<br/>                                                                        |
| <span id="PICTYPE_BITMAP"></span><span id="pictype_bitmap"></span><dl> <dt>**PICTYPE \_ BITMAP**</dt> <dt>1</dt> </dl>                         | Il tipo di immagine è una bitmap. Quando questo valore si verifica nella struttura [**PICTDESC**](/windows/win32/api/olectl/ns-olectl-pictdesc) , significa che il campo **BMP** della struttura contiene i parametri di inizializzazione pertinenti.<br/>             |
| <span id="PICTYPE_METAFILE"></span><span id="pictype_metafile"></span><dl> <dt>**PICTYPE \_ METAFILE**</dt> <dt>2</dt> </dl>                   | Il tipo di immagine è un metafile. Quando questo valore si verifica nella struttura [**PICTDESC**](/windows/win32/api/olectl/ns-olectl-pictdesc) , significa che il campo **WMF** della struttura contiene i parametri di inizializzazione pertinenti.<br/>           |
| <span id="PICTYPE_ICON"></span><span id="pictype_icon"></span><dl> <dt>**PICTYPE \_ ICONA**</dt> <dt>3</dt> </dl>                               | Il tipo di immagine è un'icona. Quando questo valore si verifica nella struttura [**PICTDESC**](/windows/win32/api/olectl/ns-olectl-pictdesc) , significa che il campo **icona** della struttura contiene i parametri di inizializzazione pertinenti.<br/>             |
| <span id="PICTYPE_ENHMETAFILE"></span><span id="pictype_enhmetafile"></span><dl> <dt>**PICTYPE \_ ENHMETAFILE**</dt> <dt>4</dt> </dl>          | Il tipo di immagine è un metafile avanzato. Quando questo valore si verifica nella struttura [**PICTDESC**](/windows/win32/api/olectl/ns-olectl-pictdesc) , significa che il campo **EMF** della struttura contiene i parametri di inizializzazione pertinenti.<br/> |



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                          |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                |
| Intestazione<br/>                   | <dl> <dt>OleCtl. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Tipo IPicture:: Get \_**](/windows/desktop/api/OCIdl/nf-ocidl-ipicture-get_type)
</dt> <dt>

[**OleCreatePictureIndirect**](/windows/desktop/api/OleCtl/nf-olectl-olecreatepictureindirect)
</dt> <dt>

[**PICTDESC**](/windows/win32/api/olectl/ns-olectl-pictdesc)
</dt> </dl>

 

 





