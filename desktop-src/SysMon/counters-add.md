---
title: Metodo Counters. Add
description: Aggiunge un'istanza di CounterItem alla raccolta.
ms.assetid: 9daecfe6-c2a9-48af-8b59-4f81f0325535
keywords:
- Aggiungere il metodo SysMon
- Add Method SysMon, classe Counters
- Classe contatori SysMon, Aggiungi metodo
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
ms.openlocfilehash: 7e6c974c5df6f531cd75292290c61534a923e5be
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104475827"
---
# <a name="countersadd-method"></a>Metodo Counters. Add

Aggiunge un'istanza di [**CounterItem**](counteritem.md) alla raccolta.

## <a name="syntax"></a>Sintassi


```VB
Counters.Add( _
  ByVal pathname As String _
) As CounterItem
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*nome percorso* \[ in\]
</dt> <dd>

Percorso del contatore. Il percorso può includere un nome di computer e deve includere il nome di un oggetto prestazione, il nome di un'istanza dell'oggetto se l'oggetto prestazione specificato supporta più istanze e il nome di un contatore. Questa specifica del percorso non distingue tra maiuscole e minuscole.

Per informazioni dettagliate su come specificare un percorso del contatore, vedere [specifica di un percorso del contatore](/windows/desktop/PerfCtrs/specifying-a-counter-path).

</dd> </dl>

## <a name="exceptions"></a>Eccezioni



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Tipo di eccezione</th>
<th>Condizione</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><strong>System. Runtime. InteropServices. COMException</strong></td>
<td>È possibile ricevere questa eccezione per uno dei motivi seguenti:
<ul>
<li>L'oggetto prestazione specificato non è stato trovato nel computer. Il valore ERR. Number è 0xC0000BB8.</li>
<li>Impossibile trovare il contatore specificato. Il valore ERR. Number è 0xC0000BB9.</li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="remarks"></a>Commenti

Se si specifica un contatore con caratteri jolly nel parametro *pathname* , il metodo **Add** crea un oggetto [**CounterItem**](counteritem.md) per ogni percorso espanso. Il metodo **Add** restituisce quindi un puntatore al primo **CounterItem** aggiunto.

Se il carattere jolly genera un contatore duplicato, l'errore non viene segnalato e non viene creato alcun duplicato. Se si verifica una condizione di errore prima della creazione di tutti i contatori, viene restituito l'errore e non vengono creati i restanti contatori.

Non esiste alcun limite al numero di contatori che è possibile aggiungere; Tuttavia, SYSMON creerà solo i primi 1.024 contatori della raccolta. Non esiste alcun limite al numero di contatori che SYSMON visualizzerà in un report.

Per ricevere una notifica quando viene aggiunto un contatore, implementare l'evento [OnCounterAdded](systemmonitor-oncounteradded.md) .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                            |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                  |
| DLL<br/>                      | <dl> <dt>Sysmon. ocx</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**CounterItem**](counteritem.md)
</dt> <dt>

[**Contatori**](counters.md)
</dt> <dt>

[**SystemMonitor. BrowseCounters**](systemmonitor-browsecounters.md)
</dt> </dl>

 

