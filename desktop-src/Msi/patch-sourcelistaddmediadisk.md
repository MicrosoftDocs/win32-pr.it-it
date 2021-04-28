---
description: 'Metodo Patch.SourceListAddMediaDisk: il metodo SourceListAddMediaDisk aggiunge un disco al set di dischi registrati. Accetta Diskid, VolumeLabel e DiskPrompt come parametri. Questo metodo chiama su MsiSourceListAddMediaDisk.'
ms.assetid: 6feaf2d3-7e39-4e22-9e74-9a2f98369eac
title: Metodo Patch.SourceListAddMediaDisk
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Patch.SourceListAddMediaDisk
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 052831befb95976358b53d989db36d5b2fa43efe
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108084374"
---
# <a name="patchsourcelistaddmediadisk-method"></a>Metodo Patch.SourceListAddMediaDisk

Il **metodo SourceListAddMediaDisk** aggiunge un disco al set di dischi registrati. Accetta *Diskid,* *VolumeLabel e* *DiskPrompt* come parametri. Questo metodo chiama su [**MsiSourceListAddMediaDisk.**](/windows/desktop/api/Msi/nf-msi-msisourcelistaddmediadiska)

## <a name="syntax"></a>Sintassi


```JScript
Patch.SourceListAddMediaDisk(
  Diskid,
  VolumeLabel,
  DiskPrompt
)
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Diskid* 
</dt> <dd>

Questo parametro fornisce l'ID del disco da aggiungere o aggiornare.

</dd> <dt>

*VolumeLabel* 
</dt> <dd>

Questo parametro fornisce l'etichetta del disco da aggiungere o aggiornare. Un aggiornamento sovrascrive l'etichetta di volume esistente nel Registro di sistema. Per modificare solo il prompt del disco, ottenere l'etichetta del volume registrato esistente e specificarla insieme al prompt del nuovo disco. Una stringa NULL o vuota registra una stringa vuota (lunghezza di 0 byte) come etichetta di volume.

</dd> <dt>

*DiskPrompt* 
</dt> <dd>

Questo parametro fornisce la richiesta del disco per l'aggiunta o l'aggiornamento del disco. Un aggiornamento sovrascrive il prompt del disco esistente nel Registro di sistema. Per modificare solo l'etichetta di volume, ottenere il prompt del disco esistente dal Registro di sistema e fornire la nuova etichetta di volume. Una stringa NULL o vuota registra una stringa vuota (lunghezza di 0 byte) come richiesta del disco.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versione<br/> | Windows Installer 5.0 in Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Installer 4.0 o Windows Installer 4.5 in Windows Server 2008 o Windows Vista. Windows Installer 3.0 o versione successiva in Windows Server 2003, Windows XP e Windows 2000<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                                                   |
| IID<br/>     | IPatch IID è definito come \_ 000C10A1-0000-0000-C000-000000000046<br/>                                                                                                                                                                                                            |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Patch**](patch-object.md)
</dt> <dt>

[**MsiSourceListAddMediaDisk**](/windows/desktop/api/Msi/nf-msi-msisourcelistaddmediadiska)
</dt> <dt>

[Non supportato in Windows Installer 2.0 e versioni precedenti](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 




