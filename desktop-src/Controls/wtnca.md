---
title: Valori WTNCA (Uxtheme.h)
description: Specifica i flag che modificano gli attributi dello stile di visualizzazione della finestra. Utilizzare uno o una combinazione bit per bit dei valori seguenti.
ms.assetid: C71D1957-6572-4242-B715-C54BDFBBD6B7
topic_type:
- apiref
api_name:
- WTNCA_NODRAWCAPTION
- WTNCA_NODRAWICON
- WTNCA_NOSYSMENU
- WTNCA_NOMIRRORHELP
- WTNCA_VALIDBITS
api_location:
- Uxtheme.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3b5528e26b7dc24a744affad84c8fd1fe74607ed1af56e20651fd43723cdbbff
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120059291"
---
# <a name="wtnca-values"></a>Valori WTNCA

Specifica i flag che modificano gli attributi dello stile di visualizzazione della finestra. Utilizzare uno o una combinazione bit per bit dei valori seguenti.



| Costante/valore                                                                                                                                                                                                                                  | Descrizione                                                                             |
|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------|
| <span id="WTNCA_NODRAWCAPTION"></span><span id="wtnca_nodrawcaption"></span><dl> <dt>**WTNCA \_ NoDRAWCAPTION**</dt> <dt>0x00000001</dt> </dl> | Impedisce di disegnare la didascalia della finestra.<br/>                                |
| <span id="WTNCA_NODRAWICON"></span><span id="wtnca_nodrawicon"></span><dl> <dt>**WTNCA \_ NoDRAWICON**</dt> <dt>0x00000002</dt> </dl>          | Impedisce di disegnare l'icona di sistema.<br/>                                   |
| <span id="WTNCA_NOSYSMENU"></span><span id="wtnca_nosysmenu"></span><dl> <dt>**WTNCA \_ NoSYSMENU**</dt> <dt>0x00000004</dt> </dl>             | Impedisce la visualizzazione del menu icona di sistema.<br/>                                |
| <span id="WTNCA_NOMIRRORHELP"></span><span id="wtnca_nomirrorhelp"></span><dl> <dt>**WTNCA \_ NOMIRRORHELP**</dt> <dt>0x00000008</dt> </dl>    | Impedisce il mirroring del punto interrogativo, anche nel layout da destra a sinistra (RTL).<br/> |
| <span id="WTNCA_VALIDBITS"></span><span id="wtnca_validbits"></span><dl> <dt>**VALIDBIT WTNCA \_**</dt> </dl>                                                                             | Maschera che contiene tutti i bit validi.<br/>                                     |



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>                                       |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2008 \[\]<br/>                                 |
| Intestazione<br/>                   | <dl> <dt>Uxtheme.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

**Riferimento**
</dt> <dt>

[**OPZIONI \_ WTA**](/windows/desktop/api/Uxtheme/ns-uxtheme-wta_options)
</dt> <dt>

[**SetWindowThemeNonClientAttributes**](/windows/desktop/api/Uxtheme/nf-uxtheme-setwindowthemenonclientattributes)
</dt> </dl>

 

 





