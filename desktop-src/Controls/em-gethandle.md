---
title: EM_GETHANDLE messaggio (Winuser.h)
description: Ottiene un handle della memoria attualmente allocata per il testo di un controllo di modifica su più righe.
ms.assetid: 74271812-9715-4a46-96b3-0788134f8143
keywords:
- EM_GETHANDLE dei messaggi Windows controlli
topic_type:
- apiref
api_name:
- EM_GETHANDLE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4f09ade5545197df2dbc9310b708cd7521334bba68f41a14329dd865e84fdee6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119019649"
---
# <a name="em_gethandle-message"></a>Messaggio \_ EM GETHANDLE

Ottiene un handle della memoria attualmente allocata per il testo di un controllo di modifica su più righe.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Non usato; deve essere zero.

</dd> <dt>

*lParam* 
</dt> <dd>

Non usato; deve essere zero.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il valore restituito è un handle di memoria che identifica il buffer che contiene il contenuto del controllo di modifica. Se si verifica un errore, ad esempio l'invio del messaggio a un controllo di modifica a riga singola, il valore restituito è zero.

## <a name="remarks"></a>Commenti

Se la funzione ha esito positivo, l'applicazione può accedere al contenuto del controllo di modifica eseguendo il cast del valore restituito a [**HLOCAL**](/windows/desktop/WinProg/windows-data-types) e passandolo a [**LocalLock**](/windows/desktop/api/winbase/nf-winbase-locallock). **LocalLock** restituisce un puntatore a un buffer che è una matrice con terminazione Null di **CHAR** s o **WCHAR,** a seconda che il controllo sia stato creato da una funzione ANSI o Unicode. Ad esempio, se è stato usato [**CreateWindowExA,**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) il buffer è una matrice di **CHAR,** ma se è stato usato **CreateWindowExW,** il buffer è una matrice **di WCHAR.** L'applicazione non può modificare il contenuto del buffer. Per sbloccare il buffer, l'applicazione chiama [**LocalUnlock**](/windows/desktop/api/winbase/nf-winbase-localunlock) prima di consentire al controllo di modifica di ricevere nuovi messaggi.

> [!Note]  
> Ad Comctl32.dll versione 6, il buffer contiene sempre una matrice di **WCHAR,** indipendentemente dal fatto che una funzione ANSI o Unicode ha creato il controllo di modifica. Per altre informazioni sulle versioni delle DLL, vedere [Versioni comuni del controllo](common-control-versions.md).

 

Se l'applicazione non può rispettare le restrizioni imposte da **EM \_ GETHANDLE,** usare le funzioni [**GetWindowTextLength**](/windows/desktop/api/winuser/nf-winuser-getwindowtextlengtha) e [**GetWindowText**](/windows/desktop/api/winuser/nf-winuser-getwindowtexta) per copiare il contenuto del controllo di modifica in un buffer fornito dall'applicazione.

**Rich Edit:** Il **messaggio EM \_ GETHANDLE** non è supportato. I controlli Rich Edit non archiviano il testo come semplice matrice di caratteri.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                                           |
| Server minimo supportato<br/> | Windows Solo app desktop server 2003 \[\]<br/>                                                     |
| Intestazione<br/>                   | <dl> <dt>Winuser.h (includere Windows.h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

**Riferimento**
</dt> <dt>

[**EM \_ SETHANDLE**](em-sethandle.md)
</dt> <dt>

**Altre risorse**
</dt> <dt>

[**GetWindowText**](/windows/desktop/api/winuser/nf-winuser-getwindowtexta)
</dt> <dt>

[**GetWindowTextLength**](/windows/desktop/api/winuser/nf-winuser-getwindowtextlengtha)
</dt> <dt>

[**LocalLock**](/windows/desktop/api/winbase/nf-winbase-locallock)
</dt> <dt>

[**LocalUnlock**](/windows/desktop/api/winbase/nf-winbase-localunlock)
</dt> </dl>

 

