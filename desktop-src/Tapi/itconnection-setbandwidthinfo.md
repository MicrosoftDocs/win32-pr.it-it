---
description: Il metodo SetBandwidthInfo imposta le informazioni sulla larghezza di banda.
ms.assetid: bf5db456-ea67-4a65-a681-df0741f73fc9
title: 'Metodo ITConnection:: SetBandwidthInfo (sdpblb. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5c17054743f6d47775e994dbfe3b80c7afe1ab68
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326495"
---
# <a name="itconnectionsetbandwidthinfo-method"></a>Metodo ITConnection:: SetBandwidthInfo

\[ I controlli e le interfacce per la comunicazione di telefonia IP Rendezvous non sono disponibili per l'uso in Windows Vista, Windows Server 2008 e nelle versioni successive del sistema operativo. L'API del client RTC fornisce funzionalità simili.\]

Il metodo **SetBandwidthInfo** imposta le informazioni sulla larghezza di banda.

## <a name="syntax"></a>Sintassi


```C++
HRESULT SetBandwidthInfo(
  [in] BSTR   pModifier,
  [in] DOUBLE Bandwidth
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pModifier* \[ in\]
</dt> <dd>

Puntatore a un **BSTR** che indica l'ambito della larghezza di banda da impostare. Per ulteriori informazioni, vedere la sezione Osservazioni successiva.

</dd> <dt>

*Larghezza di banda* \[ in\]
</dt> <dd>

Banda.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo può restituire uno di questi valori.



| Valore                                                                                         | Significato                                                           |
|-----------------------------------------------------------------------------------------------|-------------------------------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>          | Il metodo è riuscito.<br/>                                      |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | Il parametro *pModifier* o *Bandwidth* non è valido.<br/> |
| <dl> <dt>**E \_ OutOfMemory**</dt> </dl> | La memoria disponibile non è sufficiente per eseguire l'operazione.<br/>   |
| <dl> <dt>**E \_ non riescono**</dt> </dl>        | Errore non specificato.<br/>                                     |
| <dl> <dt>**E \_ NOTIMPL**</dt> </dl>     | Questo metodo non è ancora implementato.<br/>                    |



 

## <a name="remarks"></a>Commenti

L'applicazione deve usare [**SysAllocString**](/windows/win32/api/oleauto/nf-oleauto-sysallocstring) per allocare memoria per il parametro *PModifier* e usare [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) per liberare la memoria quando la variabile non è più necessaria.

Riferimento: RFC 2327.

Il modificatore della larghezza di banda sarà in genere CT o come:

**Totale conferenza CT:** Una larghezza di banda massima implicita è associata a ogni durata (TTL) in MBone o all'interno di una particolare area dell'ambito amministrativo multicast (i limiti della larghezza [*di*](t-tapgloss.md) banda di MBone rispetto a quelli TTL sono indicati nelle domande frequenti su MBone). Se la larghezza di banda di una sessione o di un supporto in una sessione è diversa dalla larghezza di banda implicita dall'ambito, a \` b = CT:.. .' la riga deve essere fornita per la sessione, assegnando il limite superiore proposto alla larghezza di banda usata. Lo scopo principale di questa operazione è fornire un'idea approssimativa del modo in cui due o più conferenze possono coesistere simultaneamente.

**Come Application-Specific massimo:** La larghezza di banda viene interpretata come specifica dell'applicazione, ad esempio, sarà il concetto di larghezza di banda massima dell'applicazione. Normalmente questo coincide con quello impostato sul controllo "larghezza di banda massima" dell'applicazione, se applicabile.

Si noti che CT fornisce una cifra della larghezza di banda totale per tutti i supporti in tutti i siti. Come fornisce una quantità di larghezza di banda per un singolo supporto in un singolo sito, anche se possono essere presenti più siti che inviano simultaneamente.

**Meccanismo di estensione:** I writer di strumenti possono definire modificatori della larghezza di banda sperimentali anteponendo i modificatori con "X-".

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------|---------------------------------------------------------------------------------------|
| Versione TAPI<br/> | Richiede TAPI 3,0 o versione successiva<br/>                                                 |
| Intestazione<br/>       | <dl> <dt>Sdpblb. h</dt> </dl>   |
| Libreria<br/>      | <dl> <dt>UUID. lib</dt> </dl>   |
| DLL<br/>          | <dl> <dt>Sdpblb.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**ITConnection**](itconnection.md)
</dt> </dl>

 

