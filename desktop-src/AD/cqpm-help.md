---
title: Messaggio CQPM_HELP (cmnquery. h)
description: Inviato alla funzione di callback CQPageProc di una pagina di estensione del modulo di query per consentire all'estensione di pagina di visualizzare la Guida sensibile al contesto per la pagina.
ms.assetid: 07f5bd24-bca2-4d87-8e1e-acce552a3bf2
ms.tgt_platform: multiple
keywords:
- Messaggio CQPM_HELP Active Directory
topic_type:
- apiref
api_name:
- CQPM_HELP
api_location:
- Cmnquery.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7635b87a0ba489c63f87fb32742c37a9f7044860
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104119171"
---
# <a name="cqpm_help-message"></a>\_Messaggio della Guida CQPM

Il messaggio della **\_ Guida CQPM** viene inviato alla funzione di callback [**CQPageProc**](/windows/desktop/api/Cmnquery/nc-cmnquery-lpcqpageproc) di una pagina di estensione del modulo di query per consentire all'estensione di pagina di visualizzare la Guida sensibile al contesto per la pagina. Se possibile, l'estensione della pagina query dovrebbe visualizzare la Guida sensibile al contesto in risposta a questo evento.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Non usato.

</dd> <dt>

*lParam* 
</dt> <dd>

Puntatore a una struttura [**HELPINFO**](/windows/win32/api/winuser/ns-winuser-helpinfo) contenente dati aggiuntivi relativi alla voce di menu, al controllo, alla finestra di dialogo o alla finestra per la quale è richiesta la Guida sensibile al contesto.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il valore restituito per questo messaggio viene ignorato.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>                                                              |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                        |
| Intestazione<br/>                   | <dl> <dt>Cmnquery. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**CQPageProc**](/windows/desktop/api/Cmnquery/nc-cmnquery-lpcqpageproc)
</dt> <dt>

[**HELPINFO**](/windows/win32/api/winuser/ns-winuser-helpinfo)
</dt> </dl>

 

