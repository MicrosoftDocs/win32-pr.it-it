---
title: LB_ADDFILE messaggio (Winuser.h)
description: Aggiunge il nome file specificato a una casella di riepilogo che contiene un elenco di directory.
ms.assetid: 60426293-779b-4a4b-95a2-4901b5f6a13b
keywords:
- LB_ADDFILE dei controlli Windows messaggio
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
ms.openlocfilehash: 8077bda3015fef36d6383f37f272ddaf25469fcb6930bb38bd0fa8122efc5b55
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119434481"
---
# <a name="lb_addfile-message"></a>Messaggio \_ ADDFILE di LB

Aggiunge il nome file specificato a una casella di riepilogo che contiene un elenco di directory.

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

Il valore restituito è l'indice in base zero del file aggiunto o LB \_ ERR se si verifica un errore.

## <a name="remarks"></a>Commenti

La casella di riepilogo a *cui viene aggiunto lParam* deve essere stata compilata dalla [**funzione DlgDirList.**](/windows/desktop/api/Winuser/nf-winuser-dlgdirlista)

Il [**messaggio \_ LB INITSTORAGE**](lb-initstorage.md) consente di velocizzare l'inizializzazione delle caselle di riepilogo con un numero elevato di elementi (più di 100). Riserva la quantità di memoria specificata in modo che i messaggi **\_ ADDFILE LB** successivi prendano il tempo più breve possibile. È possibile usare stime per i *parametri wParam* *e lParam.* Se si sovrastima, viene allocata memoria aggiuntiva. Se si sottovaluta, l'allocazione normale viene usata per gli elementi che superano la quantità richiesta.

Per un'applicazione ANSI, il sistema converte il testo in una casella di riepilogo in Unicode usando CP \_ ACP. Ciò può causare problemi. Ad esempio, i caratteri romani accentati in una casella di riepilogo non Unicode in giapponese Windows verranno visualizzati in gran parte. Per risolvere questo problema, compilare l'applicazione come Unicode o usare una casella di riepilogo disegnata dal proprietario.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>                                                           |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2003 \[\]<br/>                                                     |
| Intestazione<br/>                   | <dl> <dt>Winuser.h (includere Windows.h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

**Riferimento**
</dt> <dt>

[**DlgDirList**](/windows/desktop/api/Winuser/nf-winuser-dlgdirlista)
</dt> <dt>

[**LB \_ ADDSTRING**](lb-addstring.md)
</dt> </dl>

 

 





