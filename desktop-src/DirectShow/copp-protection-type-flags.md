---
description: Le costanti seguenti vengono usate con il protocollo COPP (Certified Output Protocol) per i meccanismi di protezione dell'output specifici.
ms.assetid: a3cd63d8-22a5-473c-83c2-3499f3d32671
title: Flag del tipo di protezione COPP (DXVA. h)
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
ms.openlocfilehash: 57e9ccc9420659ac09c19f2bbb7a18db519c07bc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333600"
---
# <a name="copp-protection-type-flags"></a>Flag del tipo di protezione COPP

Le costanti seguenti vengono usate con il protocollo COPP (Certified Output Protocol) per i meccanismi di protezione dell'output specifici.



| Costante/valore                                                                                                                                                                                                                                                                                                             | Descrizione                                                     |
|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------|
| <span id="COPP_ProtectionType_Unknown"></span><span id="copp_protectiontype_unknown"></span><span id="COPP_PROTECTIONTYPE_UNKNOWN"></span><dl> <dt>**Copp \_ 0x80000000 \_ sconosciuto ProtectionType**</dt> <dt></dt> </dl>     | Meccanismo di protezione sconosciuto.<br/>                        |
| <span id="COPP_ProtectionType_None"></span><span id="copp_protectiontype_none"></span><span id="COPP_PROTECTIONTYPE_NONE"></span><dl> <dt>**Copp \_ ProtectionType \_ None**</dt> <dt>0x00000000</dt> </dl>                 | Nessun meccanismo di protezione.<br/>                            |
| <span id="COPP_ProtectionType_HDCP"></span><span id="copp_protectiontype_hdcp"></span><span id="COPP_PROTECTIONTYPE_HDCP"></span><dl> <dt>**Copp \_ 0x00000001 ProtectionType \_ HDCP**</dt> <dt></dt> </dl>                 | High-Bandwidth protezione del contenuto digitali (HDCP).<br/>    |
| <span id="COPP_ProtectionType_ACP"></span><span id="copp_protectiontype_acp"></span><span id="COPP_PROTECTIONTYPE_ACP"></span><dl> <dt>**Copp \_ ProtectionType \_ ACP**</dt> <dt>0x00000002</dt> </dl>                     | Protezione copia analoga (ACP).<br/>                        |
| <span id="COPP_ProtectionType_CGMSA"></span><span id="copp_protectiontype_cgmsa"></span><span id="COPP_PROTECTIONTYPE_CGMSA"></span><dl> <dt>**Copp \_ ProtectionType \_ CGMSA**</dt> <dt>0x00000004</dt> </dl>             | Sistema di gestione della generazione di copia analogico (CGMS-A).<br/> |
| <span id="COPP_ProtectionType_Mask"></span><span id="copp_protectiontype_mask"></span><span id="COPP_PROTECTIONTYPE_MASK"></span><dl> <dt>**Copp \_ ProtectionType \_ mask**</dt> <dt>0x80000007</dt> </dl>                 | Maschera di maschera per isolare i flag validi.<br/>                      |
| <span id="COPP_ProtectionType_Reserved"></span><span id="copp_protectiontype_reserved"></span><span id="COPP_PROTECTIONTYPE_RESERVED"></span><dl> <dt>**Copp \_ 0x7FFFFFF8 \_ riservato ProtectionType**</dt> <dt></dt> </dl> | Riservato. Deve essere zero.<br/>                              |



## <a name="remarks"></a>Commenti

Alcuni metodi restituiscono un flag singolo da questo tipo di enumerazione e alcuni metodi restituiscono **un operatore OR** bit per bit di uno o più flag.

Questi flag vengono usati nelle query e nei comandi COPP seguenti.

-   Livello di protezione globale
-   Livello di protezione locale
-   Tipo di protezione
-   Imposta il livello di protezione

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|-----------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>DXVA. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Costanti e GUID](constants-and-guids.md)
</dt> <dt>

[Uso di COPP (Certified Output Protocol)](using-certified-output-protection-protocol--copp.md)
</dt> </dl>

 

 




