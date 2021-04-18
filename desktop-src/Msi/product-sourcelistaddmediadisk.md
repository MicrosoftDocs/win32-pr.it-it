---
description: Il metodo SourceListAddMediaDisk aggiunge un disco al set di dischi registrati. Accetta i parametri DiskID, VolumeLabel e DiskPrompt. Questo metodo chiama su MsiSourceListAddMediaDisk.
ms.assetid: 19cb6884-2191-4da3-a6d2-8874564be67d
title: Metodo Product. SourceListAddMediaDisk
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Product.SourceListAddMediaDisk
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: d2f81b21570d708f361e45be7f6f42a93fd0d335
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325885"
---
# <a name="productsourcelistaddmediadisk-method"></a>Metodo Product. SourceListAddMediaDisk

Il metodo **SourceListAddMediaDisk** aggiunge un disco al set di dischi registrati. Accetta i parametri *DiskID*, *VolumeLabel* e *DiskPrompt* . Questo metodo chiama su [**MsiSourceListAddMediaDisk**](/windows/desktop/api/Msi/nf-msi-msisourcelistaddmediadiska).

## <a name="syntax"></a>Sintassi


```JScript
Product.SourceListAddMediaDisk(
  Diskid,
  VolumeLabel,
  DiskPrompt
)
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*DiskID* 
</dt> <dd>

Questo parametro fornisce l'ID del disco da aggiungere o aggiornare.

</dd> <dt>

*VolumeLabel* 
</dt> <dd>

Questo parametro fornisce l'etichetta del disco da aggiungere o aggiornare. Un aggiornamento sovrascrive l'etichetta di volume esistente nel registro di sistema. Per modificare solo il prompt del disco, ottenere l'etichetta del volume registrato esistente e fornirla insieme al nuovo prompt del disco. Una stringa vuota per questo parametro registra una stringa vuota (di lunghezza 0 byte) come etichetta del volume.

</dd> <dt>

*DiskPrompt* 
</dt> <dd>

Questo parametro fornisce la richiesta di disco del disco da aggiungere o aggiornare. Un aggiornamento sovrascrive il prompt del disco esistente nel registro di sistema. Per modificare solo l'etichetta del volume, ottenere la richiesta del disco esistente dal registro di sistema e fornirla con la nuova etichetta del volume. Una stringa vuota per questo parametro registra una stringa vuota (di lunghezza 0 byte) come richiesta del disco.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versione<br/> | Windows Installer 5,0 in Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Installer 4,0 o Windows Installer 4,5 in Windows Server 2008 o Windows Vista. Windows Installer 3,0 o versioni successive in Windows Server 2003, Windows XP e Windows 2000<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                                                   |
| IID<br/>     | IID \_ IProduct è definito come 000C10A0-0000-0000-C000-000000000046<br/>                                                                                                                                                                                                          |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Prodotto**](product-object.md)
</dt> <dt>

[**MsiSourceListAddMediaDisk**](/windows/desktop/api/Msi/nf-msi-msisourcelistaddmediadiska)
</dt> <dt>

[Non supportato in Windows Installer 2,0 e versioni precedenti](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 




