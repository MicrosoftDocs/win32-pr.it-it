---
title: Messaggio LB_ADDFILE (winuser. h)
description: Aggiunge il nome file specificato a una casella di riepilogo contenente un elenco di directory.
ms.assetid: 60426293-779b-4a4b-95a2-4901b5f6a13b
keywords:
- Controlli di Windows Message LB_ADDFILE
topic_type:
- apiref
api_name:
- LB_ADDFILE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 18b3d66c6a6c8495c67df2078370911ca9cd31df
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104478262"
---
# <a name="lb_addfile-message"></a>\_Messaggio AddFile lb

Aggiunge il nome file specificato a una casella di riepilogo contenente un elenco di directory.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Questo parametro non viene usato.

</dd> <dt>

*lParam* 
</dt> <dd>

Puntatore a un buffer che specifica il nome del file da aggiungere.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il valore restituito è l'indice in base zero del file che è stato aggiunto oppure LB \_ Err se si verifica un errore.

## <a name="remarks"></a>Commenti

La casella di riepilogo a cui viene aggiunto *lParam* deve essere stata compilata dalla funzione [**DlgDirList**](/windows/desktop/api/Winuser/nf-winuser-dlgdirlista) .

Il messaggio [**lb \_ INITSTORAGE**](lb-initstorage.md) consente di velocizzare l'inizializzazione di caselle di riepilogo con un numero elevato di elementi (più di 100). Si riserva la quantità di memoria specificata in modo che i messaggi **lb \_ AddFile** il tempo più breve possibile. È possibile utilizzare le stime per i parametri *wParam* e *lParam* . Se si esegue la sovrastima, viene allocata la memoria aggiuntiva. Se si sottovaluta, l'allocazione normale viene utilizzata per gli elementi che superano la quantità richiesta.

Per un'applicazione ANSI, il sistema converte il testo in una casella di riepilogo in formato Unicode usando CP \_ ACP. Ciò può causare problemi. Ad esempio, i caratteri romani accentati in una casella di riepilogo non Unicode nelle finestre giapponesi verranno disattivati. Per risolvere questo problema, compilare l'applicazione come Unicode o utilizzare una casella di riepilogo creata dal proprietario.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                                           |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                                     |
| Intestazione<br/>                   | <dl> <dt>Winuser. h (include Windows. h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

**Riferimento**
</dt> <dt>

[**DlgDirList**](/windows/desktop/api/Winuser/nf-winuser-dlgdirlista)
</dt> <dt>

[**\_ADDSTRING lb**](lb-addstring.md)
</dt> </dl>

 

 





