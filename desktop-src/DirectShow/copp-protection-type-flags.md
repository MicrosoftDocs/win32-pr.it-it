---
description: Le costanti seguenti vengono usate con il protocollo COPP (Certified Output Protection Protocol) per meccanismi di protezione dell'output specifici.
ms.assetid: a3cd63d8-22a5-473c-83c2-3499f3d32671
title: Flag del tipo di protezione COPP (Dxva.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- COPP_ProtectionType_Unknown
- COPP_ProtectionType_None
- COPP_ProtectionType_HDCP
- COPP_ProtectionType_ACP
- COPP_ProtectionType_CGMSA
- COPP_ProtectionType_Mask
- COPP_ProtectionType_Reserved
api_type:
- HeaderDef
api_location:
- dxva.h
ms.openlocfilehash: 75038b22a30be41389311fd1a7cfb830f870859b01ba48fd9a791a42cee86dc6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119214051"
---
# <a name="copp-protection-type-flags"></a>Flag del tipo di protezione COPP

Le costanti seguenti vengono usate con il protocollo COPP (Certified Output Protection Protocol) per meccanismi di protezione dell'output specifici.



| Costante/valore                                                                                                                                                                                                                                                                                                             | Descrizione                                                     |
|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------|
| <span id="COPP_ProtectionType_Unknown"></span><span id="copp_protectiontype_unknown"></span><span id="COPP_PROTECTIONTYPE_UNKNOWN"></span><dl> <dt>**COPP \_ ProtectionType \_ Unknown**</dt> <dt>0x80000000</dt> </dl>     | Meccanismo di protezione sconosciuto.<br/>                        |
| <span id="COPP_ProtectionType_None"></span><span id="copp_protectiontype_none"></span><span id="COPP_PROTECTIONTYPE_NONE"></span><dl> <dt>**COPP \_ ProtectionType \_ None**</dt> <dt>0x00000000</dt> </dl>                 | Nessun meccanismo di protezione.<br/>                            |
| <span id="COPP_ProtectionType_HDCP"></span><span id="copp_protectiontype_hdcp"></span><span id="COPP_PROTECTIONTYPE_HDCP"></span><dl> <dt>**COPP \_ ProtectionType \_ HDCP**</dt> <dt>0x00000001</dt> </dl>                 | High-Bandwidth Digital protezione del contenuto (HDCP).<br/>    |
| <span id="COPP_ProtectionType_ACP"></span><span id="copp_protectiontype_acp"></span><span id="COPP_PROTECTIONTYPE_ACP"></span><dl> <dt>**COPP \_ ProtectionType \_ ACP**</dt> <dt>0x00000002</dt> </dl>                     | Analog Copy Protection (ACP).<br/>                        |
| <span id="COPP_ProtectionType_CGMSA"></span><span id="copp_protectiontype_cgmsa"></span><span id="COPP_PROTECTIONTYPE_CGMSA"></span><dl> <dt>**COPP \_ ProtectionType \_ CGMSA**</dt> <dt>0x00000004</dt> </dl>             | Copy Generation Management System Analog (CGMS-A).<br/> |
| <span id="COPP_ProtectionType_Mask"></span><span id="copp_protectiontype_mask"></span><span id="COPP_PROTECTIONTYPE_MASK"></span><dl> <dt>**COPP \_ Maschera \_ ProtectionType**</dt> <dt>0x80000007</dt> </dl>                 | Maschera di bit per isolare i flag validi.<br/>                      |
| <span id="COPP_ProtectionType_Reserved"></span><span id="copp_protectiontype_reserved"></span><span id="COPP_PROTECTIONTYPE_RESERVED"></span><dl> <dt>**COPP \_ ProtectionType \_ Reserved**</dt> <dt>0x7FFFFFF8</dt> </dl> | Riservato. Deve essere zero.<br/>                              |



## <a name="remarks"></a>Commenti

Alcuni metodi restituiscono un singolo flag da questo tipo di enumerazione e alcuni metodi restituiscono **un'operazione OR** bit per bit di uno o più flag.

Questi flag vengono usati nei comandi e nelle query COPP seguenti.

-   Livello di protezione globale
-   Livello di protezione locale
-   Tipo di protezione
-   Impostare il livello di protezione

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|-----------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>Dxva.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Costanti e GUID](constants-and-guids.md)
</dt> <dt>

[Uso del protocollo COPP (Certified Output Protection Protocol)](using-certified-output-protection-protocol--copp.md)
</dt> </dl>

 

 




