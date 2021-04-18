---
title: Metodo SystemMonitor. SaveAs
description: Salva i valori dei contatori nella visualizzazione grafico in un file di log.
ms.assetid: 34824c54-d8f4-4c2b-b417-aa0914c7164b
keywords:
- Metodo SaveAs SysMon
- Metodo SaveAs SysMon, oggetto SystemMonitor
- Oggetto SystemMonitor SysMon, metodo SaveAs
topic_type:
- apiref
api_name:
- SystemMonitor.SaveAs
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 29c6eee811a27ba295f9c6bc5c2adb20d7b715e6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301572"
---
# <a name="systemmonitorsaveas-method"></a>Metodo SystemMonitor. SaveAs

Salva i valori dei contatori nella visualizzazione grafico in un file di log.

## <a name="syntax"></a>Sintassi


```VB
SystemMonitor.SaveAs( _
  ByVal fileName As String, _
  ByVal fileType As SysmonFileType _
)
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*nome file* \[ in\]
</dt> <dd>

Percorso del file di log. È possibile specificare il percorso come percorso assoluto, relativo o UNC. L'estensione del nome del file di log deve essere. TSV o. htm. Se una cartella nel percorso non esiste, verrà creata da SYSMON. Se il file esiste, il file viene sovrascritto. SYSMON applica gli ACL predefiniti dalla directory padre.

</dd> <dt>

*FileType* \[ in\]
</dt> <dd>

Formato dei dati del contatore salvati nel file di log. È possibile specificare [**SysmonFileType.sysmonFileHtml**](/windows/win32/api/isysmon/ne-isysmon-sysmonfiletype) o **SysmonFileType.sysmonFileTsv**.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori.

## <a name="remarks"></a>Commenti

Vengono salvati solo i dati del contatore visibili nella visualizzazione grafico (per il numero effettivo di punti dati salvati, vedere [**SystemMonitor. DataPointCount**](systemmonitor-datapointcount.md)).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/>                                  |
| DLL<br/>                      | <dl> <dt>Sysmon. ocx</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**SystemMonitor**](systemmonitor.md)
</dt> <dt>

[**SystemMonitor. relog**](systemmonitor-relog.md)
</dt> </dl>

 

 





