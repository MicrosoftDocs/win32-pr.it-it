---
title: Messaggio di EM_SETLANGOPTIONS (RichEdit. h)
description: Imposta le opzioni per l'IME (Input Method Editor) e il supporto della lingua asiatica in un controllo Rich Edit.
ms.assetid: d42d0512-3339-471d-a91a-114151554799
keywords:
- Controlli di Windows Message EM_SETLANGOPTIONS
topic_type:
- apiref
api_name:
- EM_SETLANGOPTIONS
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2e5095c599dfa78740ce4cb081e4d52c33b2debd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964118"
---
# <a name="em_setlangoptions-message"></a>\_Messaggio SETLANGOPTIONS em

Imposta le opzioni per l'IME (Input Method Editor) e il supporto della lingua asiatica in un controllo Rich Edit.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Questo parametro non viene utilizzato. deve essere zero.

</dd> <dt>

*lParam* 
</dt> <dd>

Specifica le opzioni della lingua. Per un elenco di valori possibili, vedere [**em \_ GETLANGOPTIONS**](em-getlangoptions.md).

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo messaggio restituisce un valore pari a 1.

## <a name="remarks"></a>Commenti

Il **messaggio \_ SETLANGOPTIONS em** controlla quanto segue:

-   Associazione automatica dei tipi di carattere.
-   Cambio automatico di tastiera.
-   Regolazione automatica delle dimensioni del carattere.
-   Uso dei tipi di carattere predefiniti dell'interfaccia utente anziché dei tipi di carattere predefiniti del documento.
-   Notifiche al client durante la composizione dell'IME.
-   Modo in cui IME interrompe la modalità di composizione.
-   Controllo ortografico, correzione automatica e stima della tastiera touch.

Questo messaggio consente di impostare i valori di tutti i flag di opzione della lingua. Per modificare un subset dei flag, inviare il messaggio [**\_ GETLANGOPTIONS em**](em-getlangoptions.md) per ottenere i flag di opzione correnti, modificare i flag che è necessario modificare, quindi inviare il messaggio **\_ SETLANGOPTIONS em** con il risultato.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>RichEdit. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_GETLANGOPTIONS em**](em-getlangoptions.md)
</dt> </dl>

 

 





