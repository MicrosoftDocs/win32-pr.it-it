---
title: Struttura MCI_VCR_STATUS_PARMS (VCR. h)
description: La \_ \_ struttura parametri di stato VCR MCI contiene i \_ parametri per il \_ comando di stato MCI per i registratori di cassette video.
ms.assetid: 5d7cbb64-a81d-4bdd-8f07-8c20dd7b9ef5
keywords:
- Struttura MCI_VCR_STATUS_PARMS di Windows Multimedia
topic_type:
- apiref
api_name:
- MCI_VCR_STATUS_PARMS
api_location:
- Vcr.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d0b197acfa0e170a9ab199cd6d6c51a64e14c320
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103963827"
---
# <a name="mci_vcr_status_parms-structure"></a>\_ \_ Struttura parametri stato VCR MCI \_

La **struttura \_ \_ \_ parametri di stato VCR MCI** contiene i parametri per il comando di [**\_ stato MCI**](mci-status.md) per i registratori di cassette video.

## <a name="syntax"></a>Sintassi


```C++
typedef struct tagMCI_VCR_STATUS_PARMS {
  DWORD_PTR dwCallback;
  DWORD     dwReturn;
  DWORD     dwItem;
  DWORD     dwTrack;
  DWORD     dwNumber;
} MCI_VCR_STATUS_PARMS;
```



## <a name="members"></a>Members

<dl> <dt>

**dwCallback**
</dt> <dd>

La parola di ordine inferiore specifica un handle di finestra utilizzato per il \_ flag di notifica MCI.

</dd> <dt>

**dwReturn**
</dt> <dd>

Valore restituito dal comando [**MCI \_ status**](mci-status.md) . Il valore restituito varia a seconda dell'indagine del comando. Per ulteriori informazioni, vedere la descrizione del comando [**MCI \_ status**](mci-status-parms.md) .

</dd> <dt>

**dwItem**
</dt> <dd>

Tipo di informazioni richieste.

</dd> <dt>

**dwTrack**
</dt> <dd>

Traccia audio o video che archivia le informazioni durante la registrazione successiva. Questo membro viene usato per restituire informazioni quando il comando di [**\_ stato MCI**](mci-status-parms.md) chiede lo stato di registrazione video o audio.

</dd> <dt>

**dwNumber**
</dt> <dd>

Tuner logico a cui è associato il canale corrente. Questo membro viene usato per restituire informazioni quando il comando di [**\_ stato MCI**](mci-status.md) chiede informazioni sul numero di canale corrente.

</dd> </dl>

## <a name="remarks"></a>Commenti

Quando si assegnano dati ai membri di questa struttura, impostare i flag corrispondenti nel parametro *fdwCommand* della funzione [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) per convalidare i membri.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                       |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                             |
| Intestazione<br/>                   | <dl> <dt>VCR. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**MCI**](mci.md)
</dt> <dt>

[**Strutture MCI**](mci-structures.md)
</dt> <dt>

[**\_stato MCI**](mci-status.md)
</dt> <dt>

[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))
</dt> </dl>

 

