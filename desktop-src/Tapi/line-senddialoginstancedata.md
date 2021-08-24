---
description: Il messaggio TSPI LINE SENDDIALOGINSTANCEDATA fa in modo che TAPI chiami la funzione TUISPI providerGenericDialogData nella DLL dell'interfaccia utente associata a \_ htDlgInst, passando il blocco di parametri a cui punta \_ lpParams, di lunghezza dwSize.
ms.assetid: d3c176ba-8b4b-4b7c-a603-130dfa761898
title: LINE_SENDDIALOGINSTANCEDATA messaggio (Tspi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8b955d890c385894467fa0f8f3f93ec50856c746c72f0957ecbe33af203917bf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119140134"
---
# <a name="line_senddialoginstancedata-message"></a>MESSAGGIO LINE \_ SENDDIALOGINSTANCEDATA

Il messaggio TSPI **LINE \_ SENDDIALOGINSTANCEDATA** fa in modo che TAPI chiami la funzione [**TUISPI \_ providerGenericDialogData**](/windows/win32/api/tspi/nf-tspi-tuispi_providergenericdialogdata) nella DLL dell'interfaccia utente associata a *htDlgInst,* passando il blocco di parametri a cui punta *lpParams*, di lunghezza *dwSize*.


```C++
            
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*htDlgInst* 
</dt> <dd>

HTAPIDIALOGINSTANCE restituito al provider di servizi quando l'istanza della finestra di dialogo è stata creata usando [**LINE \_ CREATEDIALOGINSTANCE.**](line-createdialoginstance.md)

</dd> <dt>

*lpParams* 
</dt> <dd>

Puntatore a un blocco di parametri specifico del provider che viene trasmesso alla funzione [**TUISPI \_ providerGenericDialogData**](/windows/win32/api/tspi/nf-tspi-tuispi_providergenericdialogdata) della DLL dell'interfaccia utente, la cui dimensione è specificata *da dwSize*. Se questo parametro è impostato su **NULL,** si tratta di una richiesta per chiudere immediatamente la finestra di dialogo ed eseguire la pulizia (la DLL dell'interfaccia utente non deve richiamare [**TUISPIDLLCALLBACK**](/windows/win32/api/tspi/nc-tspi-tuispidllcallback) durante questa pulizia).

</dd> <dt>

*dwSize* 
</dt> <dd>

Dimensione in byte del blocco di parametri da trasmettere alla DLL dell'interfaccia utente.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------|-----------------------------------------------------------------------------------|
| Versione TAPI<br/> | Richiede TAPI 2.0 o versione successiva<br/>                                             |
| Intestazione<br/>       | <dl> <dt>Tspi.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**TUISPIDLLCALLBACK**](/windows/win32/api/tspi/nc-tspi-tuispidllcallback)
</dt> <dt>

[**Provider \_ TUISPIGenericDialogData**](/windows/win32/api/tspi/nf-tspi-tuispi_providergenericdialogdata)
</dt> <dt>

[**LINE \_ CREATEDIALOGINSTANCE**](line-createdialoginstance.md)
</dt> </dl>

 

