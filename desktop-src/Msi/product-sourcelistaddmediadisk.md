---
description: 'Metodo Product.SourceListAddMediaDisk: il metodo SourceListAddMediaDisk aggiunge un disco al set di dischi registrati. Accetta Diskid, VolumeLabel e DiskPrompt come parametri. Questo metodo chiama su MsiSourceListAddMediaDisk.'
ms.assetid: 19cb6884-2191-4da3-a6d2-8874564be67d
title: Metodo Product.SourceListAddMediaDisk
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
ms.openlocfilehash: 4cf5fac906b048930b47a07acb2c04c7243d5bbf
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108113579"
---
# <a name="productsourcelistaddmediadisk-method"></a>Metodo Product.SourceListAddMediaDisk

Il **metodo SourceListAddMediaDisk** aggiunge un disco al set di dischi registrati. Accetta *Diskid,* *VolumeLabel* e *DiskPrompt* come parametri. Questo metodo chiama [**su MsiSourceListAddMediaDisk.**](/windows/desktop/api/Msi/nf-msi-msisourcelistaddmediadiska)

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

*Diskid* 
</dt> <dd>

Questo parametro fornisce l'ID del disco aggiunto o aggiornato.

</dd> <dt>

*VolumeLabel* 
</dt> <dd>

Questo parametro fornisce l'etichetta del disco da aggiungere o aggiornare. Un aggiornamento sovrascrive l'etichetta di volume esistente nel Registro di sistema. Per modificare solo il prompt del disco, ottenere l'etichetta di volume registrata esistente e specificarla insieme al nuovo prompt del disco. Una stringa vuota per questo parametro registra una stringa vuota (0 byte di lunghezza) come etichetta di volume.

</dd> <dt>

*DiskPrompt* 
</dt> <dd>

Questo parametro fornisce la richiesta su disco del disco da aggiungere o aggiornare. Un aggiornamento sovrascrive la richiesta del disco esistente nel Registro di sistema. Per modificare solo l'etichetta del volume, ottenere la richiesta del disco esistente dal Registro di sistema e specificarla con la nuova etichetta di volume. Una stringa vuota per questo parametro registra una stringa vuota (0 byte di lunghezza) come richiesta del disco.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versione<br/> | Windows Installer 5.0 in Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Installer 4.0 o Windows Installer 4.5 in Windows Server 2008 o Windows Vista. Windows Installer 3.0 o versione successiva in Windows Server 2003, Windows XP e Windows 2000<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                                                   |
| IID<br/>     | IID \_ IProduct è definito come 000C10A0-0000-0000-C000-000000000046<br/>                                                                                                                                                                                                          |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Prodotto**](product-object.md)
</dt> <dt>

[**MsiSourceListAddMediaDisk**](/windows/desktop/api/Msi/nf-msi-msisourcelistaddmediadiska)
</dt> <dt>

[Non supportato in Windows Installer 2.0 e versioni precedenti](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 




