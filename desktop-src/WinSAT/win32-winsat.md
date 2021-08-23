---
title: Win32_WinSAT classe
description: Definisce le informazioni di valutazione di riepilogo per la valutazione formale più recente.
ms.assetid: adf4de42-9dfd-46a7-ae75-3bbcfd15dd68
keywords:
- Win32_WinSAT classe WinSAT
- Win32_WinSAT classe WinSAT , descritta
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
ms.openlocfilehash: c0a9e863bd22cebc6609e32521b85de4bca29ae048d9673e3b09cfff2b95408f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119504531"
---
# <a name="win32_winsat-class"></a>Classe \_ WinSAT Win32

\[**Win32 \_ WinSAT può** essere modificato o non disponibile per le versioni dopo Windows 8.1.\]

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

La **classe Win32 \_ WinSAT** ha questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La **classe \_ WinSAT Win32** ha queste proprietà.

<dl> <dt>

**CPUScore**
</dt> <dd> <dl> <dt>

Tipo di dati: **real32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Punteggio per i processori nel computer.

</dd> <dt>

**D3DScore**
</dt> <dd> <dl> <dt>

Tipo di dati: **real32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Dopo Windows 8.1, WinSAT non valuta più le funzionalità di grafica tridimensionale (giochi) del computer e la capacità del driver di grafica di eseguire il rendering di oggetti ed eseguire shader usando questa valutazione. Per motivi di compatibilità, WinSAT segnala i valori sentinel per le metriche e i punteggi, ma non vengono calcolati in tempo reale.

</dd> <dt>

**DiskScore**
</dt> <dd> <dl> <dt>

Tipo di dati: **real32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Punteggio per la velocità effettiva di lettura sequenziale nel disco rigido primario del computer.

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

Punteggio per la velocità effettiva della memoria e la capacità del computer.

</dd> <dt>

**TimeTaken**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: **chiave**
</dt> </dl>

Questa proprietà deve essere impostata su "MostRecentAssessment" nella clausola WHERE della query WQL.

</dd> <dt>

**WinSATAssessmentState**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Stato della valutazione. Per una descrizione dei valori possibili, vedere [**l'enumerazione WINSAT \_ ASSESSMENT \_ STATE.**](/windows/win32/api/winsatcominterfacei/ne-winsatcominterfacei-winsat_assessment_state)

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

Punteggio di base per il computer. Per informazioni dettagliate sul valore del punteggio, vedere [**la proprietà IProvideWinSATResultsInfo::SystemRating.**](/windows/desktop/api/Winsatcominterfacei/nf-winsatcominterfacei-iprovidewinsatresultsinfo-get_systemrating)

</dd> </dl>

## <a name="remarks"></a>Commenti

Per informazioni sui punteggi del sottocomponente, ad esempio **MemoryScore,** vedere la [**proprietà IProvideWinSATAssessmentInfo::Score.**](/windows/desktop/api/Winsatcominterfacei/nf-winsatcominterfacei-iprovidewinsatassessmentinfo-get_score)

## <a name="examples"></a>Esempio

Per un esempio che illustra come usare WMI per recuperare dati da questa classe, vedere il metodo [**IProvideWinSATVisuals::get \_ Bitmap.**](/windows/desktop/api/Winsatcominterfacei/nf-winsatcominterfacei-iprovidewinsatvisuals-get_bitmap)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                           |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                                |
| Spazio dei nomi<br/>                | Root\\CIMv2<br/>                                                                   |
| MOF<br/>                      | <dl> <dt>WinSAT.mof</dt> </dl>    |
| DLL<br/>                      | <dl> <dt>WinSATAPI.dll</dt> </dl> |



 

 





