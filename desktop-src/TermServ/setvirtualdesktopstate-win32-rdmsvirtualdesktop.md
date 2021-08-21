---
title: Metodo SetVirtualDesktopState della classe Win32_RDMSVirtualDesktop
description: Aggiorna lo stato del desktop virtuale.
ms.assetid: 8f4f3d31-0434-4018-a33a-2ffd62c09669
ms.tgt_platform: multiple
keywords:
- Metodo SetVirtualDesktopState Servizi Desktop remoto
- Metodo SetVirtualDesktopState Servizi Desktop remoto , Win32_RDMSVirtualDesktop classe
- Win32_RDMSVirtualDesktop classe Servizi Desktop remoto, metodo SetVirtualDesktopState
topic_type:
- apiref
api_name:
- Win32_RDMSVirtualDesktop.SetVirtualDesktopState
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8b970f70996d5052674949f7ae6c89d71cbf69dc0ac90df46caaf975f8a1e279
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119058439"
---
# <a name="setvirtualdesktopstate-method-of-the-win32_rdmsvirtualdesktop-class"></a>Metodo SetVirtualDesktopState della classe \_ RDMSVirtualDesktop Win32

Aggiorna lo stato del desktop virtuale.

## <a name="syntax"></a>Sintassi


```mof
uint32 SetVirtualDesktopState(
  [in] uint32 VMState
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*VMState* \[ Pollici\]
</dt> <dd>

Valore che specifica il nuovo stato della macchina virtuale.

Questo parametro può essere impostato su uno dei valori seguenti:

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto** (0 (impostazione predefinita))


</dt> <dd>

Impossibile determinare lo stato della macchina virtuale.

</dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Abilitato** (2)


</dt> <dd>

La macchina virtuale è in esecuzione.

</dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabilitato** (3)


</dt> <dd>

La macchina virtuale è disattivata.

</dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**In pausa** (32768)


</dt> <dd>

La macchina virtuale è sospesa.

</dd> <dt>

<span id="Suspended"></span><span id="suspended"></span><span id="SUSPENDED"></span>

<span id="Suspended"></span><span id="suspended"></span><span id="SUSPENDED"></span>**Sospeso** (32769)


</dt> <dd>

La macchina virtuale è in uno stato salvato.

</dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**A** partire da (32770)


</dt> <dd>

Avvio della macchina virtuale in corso.

</dd> <dt>

<span id="Saving"></span><span id="saving"></span><span id="SAVING"></span>

<span id="Saving"></span><span id="saving"></span><span id="SAVING"></span>**Salvataggio** (32773)


</dt> <dd>

La macchina virtuale sta salvando lo stato.

</dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**Arresto** (32774)


</dt> <dd>

La macchina virtuale è in stato di spegnimento.

</dd> <dt>

<span id="Pausing"></span><span id="pausing"></span><span id="PAUSING"></span>

<span id="Pausing"></span><span id="pausing"></span><span id="PAUSING"></span>**Sospensione** (32776)


</dt> <dd>

La macchina virtuale è in pausa.

</dd> <dt>

<span id="Resuming"></span><span id="resuming"></span><span id="RESUMING"></span>

<span id="Resuming"></span><span id="resuming"></span><span id="RESUMING"></span>**Ripresa** (32777)


</dt> <dd>

La macchina virtuale sta riprendendo da uno stato di sospensione.

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce 0 in caso di esito positivo, in caso contrario restituisce un codice di errore WMI.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Nessuno supportato<br/>                                                                   |
| Server minimo supportato<br/> | Windows Server 2012<br/>                                                              |
| Spazio dei nomi<br/>                | Rdms \\ CIMv2 \\ radice<br/>                                                                |
| MOF<br/>                      | <dl> <dt>RDManagement.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>RDMS.dll</dt> </dl>         |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Win32 \_ RDMSVirtualDesktop**](win32-rdmsvirtualdesktop.md)
</dt> </dl>

 

 





