---
description: Il messaggio della riga TSPI \_ SENDDIALOGINSTANCEDATA fa in modo che TAPI chiami la \_ funzione PROVIDERGENERICDIALOGDATA di TUISPI nella DLL dell'interfaccia utente associata a htDlgInst, passando al blocco di parametri a cui punta lpParams, di lunghezza dwSize.
ms.assetid: d3c176ba-8b4b-4b7c-a603-130dfa761898
title: Messaggio LINE_SENDDIALOGINSTANCEDATA (TSPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f0af7ae5bfc942d4408ac5ce2438cd9a88c1f1f9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332917"
---
# <a name="line_senddialoginstancedata-message"></a>\_Messaggio linea SENDDIALOGINSTANCEDATA

Il messaggio della **riga TSPI \_ SENDDIALOGINSTANCEDATA** fa in modo che TAPI chiami la funzione [**\_ providerGenericDialogData di TUISPI**](/windows/win32/api/tspi/nf-tspi-tuispi_providergenericdialogdata) nella DLL dell'interfaccia utente associata a *htDlgInst*, passando al blocco di parametri a cui punta *lpParams*, di lunghezza *dwSize*.


```C++
            
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*htDlgInst* 
</dt> <dd>

HTAPIDIALOGINSTANCE restituito al provider di servizi quando l'istanza della finestra di dialogo è stata creata utilizzando la [**riga \_ CREATEDIALOGINSTANCE**](line-createdialoginstance.md).

</dd> <dt>

*lpParams* 
</dt> <dd>

Puntatore a un blocco di parametri specifico del provider trasmesso alla funzione [**TUISPI \_ PROVIDERGENERICDIALOGDATA**](/windows/win32/api/tspi/nf-tspi-tuispi_providergenericdialogdata) della DLL dell'interfaccia utente, la cui dimensione è specificata da *dwSize*. Se questo parametro è impostato su **null**, si tratta di una richiesta di chiusura immediata della finestra di dialogo e di pulizia (la DLL dell'interfaccia utente non deve richiamare [**TUISPIDLLCALLBACK**](/windows/win32/api/tspi/nc-tspi-tuispidllcallback) durante questa pulitura).

</dd> <dt>

*dwSize* 
</dt> <dd>

Dimensioni in byte del blocco di parametri da trasferire alla DLL dell'interfaccia utente.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------|-----------------------------------------------------------------------------------|
| Versione TAPI<br/> | Richiede TAPI 2,0 o versione successiva<br/>                                             |
| Intestazione<br/>       | <dl> <dt>TSPI. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**TUISPIDLLCALLBACK**](/windows/win32/api/tspi/nc-tspi-tuispidllcallback)
</dt> <dt>

[**\_PROVIDERGENERICDIALOGDATA TUISPI**](/windows/win32/api/tspi/nf-tspi-tuispi_providergenericdialogdata)
</dt> <dt>

[**LINEA \_ CREATEDIALOGINSTANCE**](line-createdialoginstance.md)
</dt> </dl>

 

