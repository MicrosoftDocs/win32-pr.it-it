---
title: Funzione RtmGetRouteAge (RTM. h)
description: La funzione RtmGetRouteAge restituisce l'età di una route. L'età è il tempo, in secondi, da quando è stato creato o ultimo aggiornamento.
ms.assetid: 93052412-227f-4c9e-978b-3ec4bde4a256
keywords:
- RAS funzione RtmGetRouteAge
topic_type:
- apiref
api_name:
- RtmGetRouteAge
api_location:
- Rtm.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a484bb5684fde974ce5fa704c0d0cca38c320851
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103742183"
---
# <a name="rtmgetrouteage-function"></a>RtmGetRouteAge (funzione)

\[Questa API è stata sostituita dall'API di [Gestione tabelle di routing versione 2](about-routing-table-manager-version-2.md) e non sarà disponibile oltre Windows Server 2003. Le applicazioni devono usare l'API di Routing Table Manager versione 2.\]

La funzione **RtmGetRouteAge** restituisce l'età di una route. L'età è il tempo, in secondi, da quando è stato creato o ultimo aggiornamento.

## <a name="syntax"></a>Sintassi


```C++
ULONG RtmGetRouteAge(
  _In_ PVOID Route
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Route* \[ in\]
</dt> <dd>

Puntatore a una struttura specifica della famiglia di protocolli che specifica i dati di route ottenuti di recente da Gestione tabelle di routing.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il valore restituito è uno dei valori seguenti.



| Valore                                                                                   | Descrizione                                                                                                                                                  |
|-----------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**Instradamento**</dt> </dl> | Tempo in secondi dall'inizio della creazione o dell'ultimo aggiornamento di una route.<br/>                                                                                    |
| <dl> <dt>**INFINITE**</dt> </dl> | Il contenuto della struttura di route non è valido. In questo caso, una chiamata a [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) restituisce l' \_ errore \_ parametro non valido.<br/> |



 

## <a name="remarks"></a>Commenti

L'età della route viene calcolata dal \_ membro del timestamp RR della struttura a cui punta il parametro di *Route* . Gestione tabelle di routing imposta il valore di questo membro quando viene aggiunta o aggiornata una route.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Nessuno supportato<br/>                                                          |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                               |
| Fine del supporto server<br/>    | Windows Server 2003<br/>                                                     |
| Intestazione<br/>                   | <dl> <dt>RTM. h</dt> </dl>   |
| Libreria<br/>                  | <dl> <dt>RTM. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Rtm.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Riferimento di gestione tabelle di routing versione \_ 1](routing-table-manager-version-1-reference.md)
</dt> <dt>

[Funzioni di Routing Table Manager versione 1](routing-table-manager-version-1-functions.md)
</dt> <dt>

[**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror)
</dt> <dt>

[**\_route IP \_ RTM**](rtm-ip-route.md)
</dt> <dt>

[**\_Route IPX \_ RTM**](rtm-ipx-route.md)
</dt> </dl>

 

