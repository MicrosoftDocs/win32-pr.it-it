---
title: Metodo Counters.Add
description: Aggiunge un'istanza CounterItem alla raccolta.
ms.assetid: 9daecfe6-c2a9-48af-8b59-4f81f0325535
keywords:
- Metodo Add SysMon
- Metodo Add SysMon , classe Counters
- Classe Counters SysMon , metodo Add
topic_type:
- apiref
api_name:
- Counters.Add
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a8d8169980de00338c7fdd0b804013f986a5a7ca
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2021
ms.locfileid: "122466008"
---
# <a name="countersadd-method"></a>Metodo Counters.Add

Aggiunge [**un'istanza CounterItem**](counteritem.md) alla raccolta.

## <a name="syntax"></a>Sintassi


```VB
Counters.Add( _
  ByVal pathname As String _
) As CounterItem
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pathname* \[ Pollici\]
</dt> <dd>

Percorso del contatore. Il percorso può includere un nome di computer e deve includere un nome di oggetto prestazioni, un nome di istanza dell'oggetto se l'oggetto prestazioni specificato supporta più istanze e un nome di contatore. Questa specifica del percorso non fa distinzione tra maiuscole e minuscole.

Per informazioni dettagliate sulla specifica di un percorso del contatore, vedere [Specifica di un percorso contatore](/windows/desktop/PerfCtrs/specifying-a-counter-path).

</dd> </dl>

## <a name="exceptions"></a>Eccezioni




| Tipo di eccezione | Condizione | 
|----------------|-----------|
| <strong>System.Runtime.InteropServices.COMException</strong> | È possibile ricevere questa eccezione per uno dei motivi seguenti:<ul><li>L'oggetto prestazioni specificato non è stato trovato nel computer. Il valore Err.Number è 0xC0000BB8.</li><li>Impossibile trovare il contatore specificato. Il valore Err.Number è 0xC0000BB9.</li></ul> | 




 

## <a name="remarks"></a>Commenti

Se si specifica un contatore con caratteri jolly nel *parametro pathname,* il **metodo Add** crea un [**oggetto CounterItem**](counteritem.md) per ogni percorso espanso. Il **metodo Add** restituisce quindi un puntatore al primo oggetto **CounterItem aggiunto.**

Se il carattere jolly comporta un contatore duplicato, l'errore non viene segnalato e non viene creato alcun duplicato. Se si verifica una condizione di errore prima della creazione di tutti i contatori, l'errore viene segnalato e i contatori rimanenti non vengono creati.

Non esiste alcun limite al numero di contatori che è possibile aggiungere. TUTTAVIA, SYSMON grafirà solo i primi 1.024 contatori nella raccolta. Non esiste alcun limite al numero di contatori che SYSMON visualizza in un report.

Per ricevere una notifica quando viene aggiunto un contatore, implementare [l'evento OnCounterAdded.](systemmonitor-oncounteradded.md)

## <a name="requirements"></a>Requisiti



| Requisito | valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                            |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                  |
| DLL<br/>                      | <dl> <dt>Sysmon.ocx</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**CounterItem**](counteritem.md)
</dt> <dt>

[**Contatori**](counters.md)
</dt> <dt>

[**SystemMonitor.BrowseCounters**](systemmonitor-browsecounters.md)
</dt> </dl>

 

