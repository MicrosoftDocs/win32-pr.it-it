---
title: Messaggio EM_GETHANDLE (winuser. h)
description: Ottiene un handle della memoria attualmente allocata per il testo di un controllo di modifica su più righe.
ms.assetid: 74271812-9715-4a46-96b3-0788134f8143
keywords:
- Controlli di Windows Message EM_GETHANDLE
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
ms.openlocfilehash: 88a466394b48d2d726621e50a7e2c5df2f747f08
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104518298"
---
# <a name="em_gethandle-message"></a>\_Messaggio GETHANDLE em

Ottiene un handle della memoria attualmente allocata per il testo di un controllo di modifica su più righe.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Non utilizzato; deve essere zero.

</dd> <dt>

*lParam* 
</dt> <dd>

Non utilizzato; deve essere zero.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il valore restituito è un handle di memoria che identifica il buffer che include il contenuto del controllo di modifica. Se si verifica un errore, ad esempio l'invio del messaggio a un controllo di modifica a riga singola, il valore restituito è zero.

## <a name="remarks"></a>Commenti

Se la funzione ha esito positivo, l'applicazione può accedere al contenuto del controllo di modifica eseguendo il cast del valore restituito a [**HLOCAL**](/windows/desktop/WinProg/windows-data-types) e passandolo a [**LocalLock**](/windows/desktop/api/winbase/nf-winbase-locallock). **LocalLock** restituisce un puntatore a un buffer che è una matrice con terminazione null di **char** s o **WCHAR** s, a seconda che una funzione ANSI o Unicode abbia creato il controllo. Se, ad esempio, è stato usato [**CreateWindowExA**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) , il buffer è una matrice di **char** s, ma se è stato usato **CreateWindowExW** , il buffer è una matrice di **WCHAR** s. È possibile che l'applicazione non modifichi il contenuto del buffer. Per sbloccare il buffer, l'applicazione chiama [**LocalUnlock**](/windows/desktop/api/winbase/nf-winbase-localunlock) prima di consentire al controllo di modifica di ricevere nuovi messaggi.

> [!Note]  
> Per Comctl32.dll versione 6, il buffer contiene sempre una matrice di **WCHAR**, indipendentemente dal fatto che una funzione ANSI o Unicode abbia creato il controllo di modifica. Per altre informazioni sulle versioni di DLL, vedere [versioni di controllo comuni](common-control-versions.md).

 

Se l'applicazione non può rispettare le restrizioni imposte da **em \_ GetHandle**, usare le funzioni [**GetWindowTextLength**](/windows/desktop/api/winuser/nf-winuser-getwindowtextlengtha) e [**GetWindowText**](/windows/desktop/api/winuser/nf-winuser-getwindowtexta) per copiare il contenuto del controllo di modifica in un buffer fornito dall'applicazione.

**Modifica avanzata:** Il **messaggio \_ GetHandle em** non è supportato. I controlli Rich Edit non archiviano il testo come una semplice matrice di caratteri.

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

[**filehandle EM \_**](em-sethandle.md)
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

 

