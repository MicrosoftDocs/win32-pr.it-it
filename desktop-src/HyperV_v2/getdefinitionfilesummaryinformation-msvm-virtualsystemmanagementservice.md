---
description: Restituisce le informazioni di riepilogo della macchina virtuale per i file di definizione della macchina virtuale specificati.
ms.assetid: 5a3d7f2c-3b89-4dd6-909d-4452afc3705f
title: Metodo GetDefinitionFileSummaryInformation della classe Msvm_VirtualSystemManagementService
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
ms.openlocfilehash: a46daedd282d07c2367931a9f20a7fbfa1849f9e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106307748"
---
# <a name="getdefinitionfilesummaryinformation-method-of-the-msvm_virtualsystemmanagementservice-class"></a>Metodo GetDefinitionFileSummaryInformation della classe MSVM \_ VirtualSystemManagementService

Restituisce le informazioni di riepilogo della macchina virtuale per i file di definizione della macchina virtuale specificati.

## <a name="syntax"></a>Sintassi


```mof
uint32 GetDefinitionFileSummaryInformation(
  [in]  string                      DefinitionFiles[],
  [out] Msvm_SummaryInformationBase SummaryInformation[]
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*DefinitionFiles* \[ in\]
</dt> <dd>

Matrice di percorsi dei file di configurazione XML per i quali restituire le informazioni di riepilogo.

</dd> <dt>

*SummaryInformation* \[ out\]
</dt> <dd>

Matrice di istanze di [**MSVM \_ SummaryInformationBase**](msvm-summaryinformation.md) contenenti le informazioni richieste per le macchine virtuali e/o gli snapshot specificati nella matrice *DefinitionFiles* . Vengono restituite solo le proprietà **Name**, **ElementName**, **creationTime** e **Notes** . tutte le altre proprietà saranno **null**.

> [!Note]  

 

Prima di Windows 10, versione 1703, DataType era [**MSVM \_ SummaryInformation**](msvm-summaryinformation.md).

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo restituisce uno dei valori seguenti.

<dl> <dt>

**Completato senza errori** (0)
</dt> <dt>

**Parametri del metodo controllati-processo avviato** (4096)
</dt> <dt>

**Non riuscito** (32768)
</dt> <dt>

**Accesso negato** (32769)
</dt> <dt>

**Non supportato** (32770)
</dt> <dt>

**Stato sconosciuto** (32771)
</dt> <dt>

**Timeout** (32772)
</dt> <dt>

**Parametro non valido** (32773)
</dt> <dt>

Il **sistema è in uso** (32774)
</dt> <dt>

**Stato non valido per l'operazione** (32775)
</dt> <dt>

**Tipo di dati non corretto** (32776)
</dt> <dt>

**Sistema non disponibile** (32777)
</dt> <dt>

**Memoria insufficiente** (32778)
</dt> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows 8\]<br/>                                                              |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2012\]<br/>                                                    |
| Spazio dei nomi<br/>                | \\Virtualizzazione radice \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_VirtualSystemManagementService MSVM**](msvm-virtualsystemmanagementservice.md)
</dt> </dl>

 

 




