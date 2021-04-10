---
title: Valori WTNCA (uxtheme. h)
description: Specifica i flag che modificano gli attributi dello stile di visualizzazione della finestra. Usare una combinazione bit per bit dei valori seguenti.
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
ms.openlocfilehash: ebaf543b688d0b403962da43029ac9aa85422bc6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104121278"
---
# <a name="wtnca-values"></a>Valori WTNCA

Specifica i flag che modificano gli attributi dello stile di visualizzazione della finestra. Usare una combinazione bit per bit dei valori seguenti.



| Costante/valore                                                                                                                                                                                                                                  | Descrizione                                                                             |
|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------|
| <span id="WTNCA_NODRAWCAPTION"></span><span id="wtnca_nodrawcaption"></span><dl> <dt>**WTNCA \_**</dt> <dt>0x00000001</dt> NODRAWCAPTION </dl> | Impedisce che venga disegnata la didascalia della finestra.<br/>                                |
| <span id="WTNCA_NODRAWICON"></span><span id="wtnca_nodrawicon"></span><dl> <dt>**WTNCA \_**</dt> <dt>0x00000002</dt> NODRAWICON </dl>          | Impedisce che venga disegnata l'icona del sistema.<br/>                                   |
| <span id="WTNCA_NOSYSMENU"></span><span id="wtnca_nosysmenu"></span><dl> <dt>**WTNCA \_**</dt> <dt>0x00000004</dt> NOSYSMENU </dl>             | Impedisce la visualizzazione del menu icona sistema.<br/>                                |
| <span id="WTNCA_NOMIRRORHELP"></span><span id="wtnca_nomirrorhelp"></span><dl> <dt>**WTNCA \_**</dt> <dt>0x00000008</dt> NOMIRRORHELP </dl>    | Impedisce il mirroring del punto interrogativo, anche nel layout da destra a sinistra (RTL).<br/> |
| <span id="WTNCA_VALIDBITS"></span><span id="wtnca_validbits"></span><dl> <dt>**\_VALIDBITS WTNCA**</dt> </dl>                                                                             | Maschera che contiene tutti i bit validi.<br/>                                     |



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                       |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/>                                 |
| Intestazione<br/>                   | <dl> <dt>Uxtheme. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

**Riferimento**
</dt> <dt>

[**\_Opzioni WTA**](/windows/desktop/api/Uxtheme/ns-uxtheme-wta_options)
</dt> <dt>

[**SetWindowThemeNonClientAttributes**](/windows/desktop/api/Uxtheme/nf-uxtheme-setwindowthemenonclientattributes)
</dt> </dl>

 

 





