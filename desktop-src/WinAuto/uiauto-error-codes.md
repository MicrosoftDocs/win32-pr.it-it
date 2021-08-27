---
title: Codici di errore (UIAutomationCoreApi.h)
description: Questo argomento descrive i codici di errore esposti da Microsoft Automazione interfaccia utente.
ms.assetid: f7820aa3-908e-426e-851c-84397019d735
topic_type:
- apiref
api_name:
- UIA_E_ELEMENTNOTAVAILABLE
- UIA_E_ELEMENTNOTENABLED
- UIA_E_INVALIDOPERATION
- UIA_E_NOCLICKABLEPOINT
- UIA_E_NOTSUPPORTED
- UIA_E_PROXYASSEMBLYNOTLOADED
- UIA_E_TIMEOUT
api_location:
- UIAutomationCoreApi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7cc0e2e9e100c8beb76b96fea85d999ed78102ff33b9827f36fc745270f0286f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118827343"
---
# <a name="error-codes-uiautomationcoreapih"></a>Codici di errore (UIAutomationCoreApi.h)

Questo argomento descrive i codici di errore esposti da Microsoft Automazione interfaccia utente. L'elenco è ordinato alfabeticamente in base al nome.



| Costante/valore                                                                                                                                                                                                                                                              | Descrizione                                                                                                                                                                                                                                              |
|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="UIA_E_ELEMENTNOTAVAILABLE"></span><span id="uia_e_elementnotavailable"></span><dl> <dt>**Interfaccia \_ utente E \_ ELEMENTNOTAVAILABLE**</dt> <dt>0x80040201</dt> </dl>          | Indica che un metodo è stato chiamato su un elemento virtualizzato o su un elemento che non esiste più, in genere perché è stato eliminato. <br/>                                                                                                  |
| <span id="UIA_E_ELEMENTNOTENABLED"></span><span id="uia_e_elementnotenabled"></span><dl> <dt>**Interfaccia \_ utente E \_ ELEMENTNOTENABLED**</dt> <dt>0x80040200</dt> </dl>                | Indica che un metodo che richiede un elemento abilitato, ad esempio [**Select**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iselectionitemprovider-select) o [**Expand,**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iexpandcollapseprovider-expand)è stato chiamato su un elemento disabilitato. <br/>             |
| <span id="UIA_E_INVALIDOPERATION"></span><span id="uia_e_invalidoperation"></span><dl> <dt>**Interfaccia \_ utente E \_ INVALIDOPERATION**</dt> <dt>0x80131509</dt> </dl>                   | Indica che il metodo ha tentato un'operazione non valida.<br/>                                                                                                                                                                          |
| <span id="UIA_E_NOCLICKABLEPOINT"></span><span id="uia_e_noclickablepoint"></span><dl> <dt>**Interfaccia \_ utente E \_ NOCLICKABLEPOINT**</dt> <dt>0x80040202</dt> </dl>                   | Indica che il [**metodo GetClickablePoint**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-getclickablepoint) è stato chiamato su un elemento che non dispone di un punto selezionabile.<br/>                                                                                    |
| <span id="UIA_E_NOTSUPPORTED"></span><span id="uia_e_notsupported"></span><dl> <dt>**Interfaccia \_ utente E \_ NOTSUPPORTED**</dt> <dt>0x80040204</dt> </dl>                               | Indica che il provider non supporta in modo esplicito la proprietà o il pattern di controllo specificato. Automazione interfaccia utente restituirà questo codice di errore al chiamante senza tentare di fornire un valore predefinito o di eseguire il falling back a un altro provider.<br/> |
| <span id="UIA_E_PROXYASSEMBLYNOTLOADED"></span><span id="uia_e_proxyassemblynotloaded"></span><dl> <dt>**Interfaccia \_ utente E \_ PROXYASSEMBLYNOTLOADED**</dt> <dt>0x80040203</dt> </dl> | Indica che si è verificato un problema durante il caricamento di un assembly che contiene un provider sul lato client (proxy).<br/>                                                                                                                                      |
| <span id="UIA_E_TIMEOUT"></span><span id="uia_e_timeout"></span><dl> <dt>**Interfaccia \_ utente E \_ TIMEOUT**</dt> <dt>0x80131505</dt> </dl>                                                      | Indica che il tempo assegnato per un processo o un'operazione è scaduto.<br/>                                                                                                                                                                      |



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop XP\]<br/>                                                      |
| Server minimo supportato<br/> | Windows Solo app desktop server 2003 \[\]<br/>                                             |
| Intestazione<br/>                   | <dl> <dt>UIAutomationCoreApi.h</dt> </dl> |



 

 





