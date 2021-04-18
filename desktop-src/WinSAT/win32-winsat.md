---
title: Classe Win32_WinSAT
description: Definisce le informazioni di valutazione di riepilogo per la valutazione formale più recente.
ms.assetid: adf4de42-9dfd-46a7-ae75-3bbcfd15dd68
keywords:
- Classe Win32_WinSAT WinSAT
- Classe Win32_WinSAT WinSAT, descrizione
topic_type:
- apiref
api_name:
- Win32_WinSAT
- Win32_WinSAT.TimeTaken
- Win32_WinSAT.WinSPRLevel
- Win32_WinSAT.WinSATAssessmentState
- Win32_WinSAT.MemoryScore
- Win32_WinSAT.CPUScore
- Win32_WinSAT.DiskScore
- Win32_WinSAT.D3DScore
- Win32_WinSAT.GraphicsScore
api_location:
- WinSATAPI.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 829e5e1b3658771728aab9ef30634d90a8bc6450
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106302732"
---
# <a name="win32_winsat-class"></a>Win32 \_ WinSAT (classe)

\[**Win32 \_ WinSAT** può essere modificato o non disponibile per le versioni dopo Windows 8.1.\]

Definisce le informazioni di valutazione di riepilogo per la valutazione formale più recente.

La sintassi seguente è semplificata dal codice MOF e include tutte le proprietà ereditate.

## <a name="syntax"></a>Sintassi

``` syntax
class Win32_WinSAT
{
  string TimeTaken = "MostRecentAssessment";
  real32 WinSPRLevel;
  uint32 WinSATAssessmentState;
  real32 MemoryScore;
  real32 CPUScore;
  real32 DiskScore;
  real32 D3DScore;
  real32 GraphicsScore;
};
```

## <a name="members"></a>Members

La classe **Win32 \_ WinSAT** presenta questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La classe **Win32 \_ WinSAT** dispone di queste proprietà.

<dl> <dt>

**CPUScore**
</dt> <dd> <dl> <dt>

Tipo di dati: **real32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Punteggio per i processori del computer.

</dd> <dt>

**D3DScore**
</dt> <dd> <dl> <dt>

Tipo di dati: **real32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Dopo Windows 8.1, WinSAT non valuterà più le funzionalità di grafica tridimensionale (gioco) del computer e la capacità del driver grafico di eseguire il rendering degli oggetti e di eseguire shader mediante questa valutazione. Per compatibilità, WinSAT segnala i valori sentinella per le metriche e i punteggi, tuttavia questi non vengono calcolati in tempo reale.

</dd> <dt>

**DiskScore**
</dt> <dd> <dl> <dt>

Tipo di dati: **real32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Punteggio per la velocità effettiva di lettura sequenziale sul disco rigido primario nel computer.

</dd> <dt>

**GraphicsScore**
</dt> <dd> <dl> <dt>

Tipo di dati: **real32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Punteggio per le funzionalità grafiche del computer.

</dd> <dt>

**MemoryScore**
</dt> <dd> <dl> <dt>

Tipo di dati: **real32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Punteggio per la velocità effettiva e la capacità della memoria del computer.

</dd> <dt>

**TimeTaken**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: **chiave**
</dt> </dl>

Questa proprietà deve essere impostata su "MostRecentAssessment" nella clausola WHERE della query WQL.

</dd> <dt>

**WinSATAssessmentState**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Stato della valutazione. Per una descrizione dei valori possibili, vedere l'enumerazione [**\_ \_ dello stato di valutazione di WinSAT**](/windows/win32/api/winsatcominterfacei/ne-winsatcominterfacei-winsat_assessment_state) .

<dl> <dt>

<span id="StateUnknown"></span><span id="stateunknown"></span><span id="STATEUNKNOWN"></span>**StateUnknown** (0)
</dt> <dt>

<span id="Valid"></span><span id="valid"></span><span id="VALID"></span>**Valido** (1)
</dt> <dt>

<span id="IncoherentWithHardware"></span><span id="incoherentwithhardware"></span><span id="INCOHERENTWITHHARDWARE"></span>**IncoherentWithHardware** (2)
</dt> <dt>

<span id="NoAssessmentAvailable"></span><span id="noassessmentavailable"></span><span id="NOASSESSMENTAVAILABLE"></span>**NoAssessmentAvailable** (3)
</dt> <dt>

<span id="Invalid"></span><span id="invalid"></span><span id="INVALID"></span>**Non valido** (4)
</dt> </dl>

</dd> <dt>

**WinSPRLevel**
</dt> <dd> <dl> <dt>

Tipo di dati: **real32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Punteggio di base per il computer. Per informazioni dettagliate sul valore score, vedere la proprietà [**IProvideWinSATResultsInfo:: SystemRating**](/windows/desktop/api/Winsatcominterfacei/nf-winsatcominterfacei-iprovidewinsatresultsinfo-get_systemrating) .

</dd> </dl>

## <a name="remarks"></a>Commenti

Per informazioni sui punteggi dei sottocomponenti, ad esempio **MemoryScore**, vedere la proprietà [**IProvideWinSATAssessmentInfo:: Score**](/windows/desktop/api/Winsatcominterfacei/nf-winsatcominterfacei-iprovidewinsatassessmentinfo-get_score) .

## <a name="examples"></a>Esempio

Per un esempio in cui viene illustrato come utilizzare WMI per recuperare dati da questa classe, vedere il metodo [**IProvideWinSATVisuals:: Get \_ bitmap**](/windows/desktop/api/Winsatcominterfacei/nf-winsatcominterfacei-iprovidewinsatvisuals-get_bitmap) .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                           |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                                |
| Spazio dei nomi<br/>                | Root\\CIMv2<br/>                                                                   |
| MOF<br/>                      | <dl> <dt>WinSAT. mof</dt> </dl>    |
| DLL<br/>                      | <dl> <dt>WinSATAPI.dll</dt> </dl> |



 

 





