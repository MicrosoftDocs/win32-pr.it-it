---
description: Restituisce informazioni di riepilogo della macchina virtuale per i file di definizione della macchina virtuale specificati.
ms.assetid: 5a3d7f2c-3b89-4dd6-909d-4452afc3705f
title: Metodo GetDefinitionFileSummaryInformation della Msvm_VirtualSystemManagementService personalizzata
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemManagementService.GetDefinitionFileSummaryInformation
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 7c6d3da6ef920488edb7fde723880b9f53768cfd246e91d287390bb6fb02fb17
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117995298"
---
# <a name="getdefinitionfilesummaryinformation-method-of-the-msvm_virtualsystemmanagementservice-class"></a>Metodo GetDefinitionFileSummaryInformation della classe Msvm \_ VirtualSystemManagementService

Restituisce informazioni di riepilogo della macchina virtuale per i file di definizione della macchina virtuale specificati.

## <a name="syntax"></a>Sintassi


```mof
uint32 GetDefinitionFileSummaryInformation(
  [in]  string                      DefinitionFiles[],
  [out] Msvm_SummaryInformationBase SummaryInformation[]
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*File di definizione* \[ Pollici\]
</dt> <dd>

Matrice di percorsi dei file di configurazione XML per i quali restituire informazioni di riepilogo.

</dd> <dt>

*Informazioni di riepilogo* \[ Cambio\]
</dt> <dd>

Matrice di [**istanze di Msvm \_ SummaryInformationBase**](msvm-summaryinformation.md) contenente le informazioni richieste per le macchine virtuali e/o gli snapshot specificati nella *matrice DefinitionFiles.* Vengono **restituite** solo le proprietà Name, **ElementName,** **CreationTime** e **Notes,** tutte le altre proprietà saranno **Null.**

> [!Note]  

 

Prima di Windows 10 versione 1703, il tipo di dati era [**Msvm \_ SummaryInformation**](msvm-summaryinformation.md).

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo restituisce uno dei valori seguenti.

<dl> <dt>

**Completata senza errori** (0)
</dt> <dt>

**Parametri del metodo verificati - Processo avviato** (4096)
</dt> <dt>

**Non riuscito** (32768)
</dt> <dt>

**Accesso negato** (32769)
</dt> <dt>

**Non supportato** (32770)
</dt> <dt>

**Lo stato è sconosciuto** (32771)
</dt> <dt>

**Timeout** (32772)
</dt> <dt>

**Parametro non** valido (32773)
</dt> <dt>

**Il sistema è in uso** (32774)
</dt> <dt>

**Stato non valido per questa operazione** (32775)
</dt> <dt>

**Tipo di dati non** corretto (32776)
</dt> <dt>

**Il sistema non è disponibile** (32777)
</dt> <dt>

**Memoria insufficiente** (32778)
</dt> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Windows 8 solo app desktop\]<br/>                                                              |
| Server minimo supportato<br/> | \[Windows Server 2012 solo app desktop\]<br/>                                                    |
| Spazio dei nomi<br/>                | Root \\ Virtualization \\ V2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Msvm \_ VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md)
</dt> </dl>

 

 




