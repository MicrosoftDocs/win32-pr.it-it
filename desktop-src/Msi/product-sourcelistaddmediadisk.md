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
ms.openlocfilehash: 9e3f6df653abeefd57f8311eed0d9e578f6a525c1a0dc915f4b629d367bb79fd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120042131"
---
# <a name="productsourcelistaddmediadisk-method"></a>Metodo Product.SourceListAddMediaDisk

Il **metodo SourceListAddMediaDisk** aggiunge un disco al set di dischi registrati. Accetta *Diskid,* *VolumeLabel* e *DiskPrompt* come parametri. Questo metodo chiama [**su MsiSourceListAddMediaDisk**](/windows/desktop/api/Msi/nf-msi-msisourcelistaddmediadiska).

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
| Versione<br/> | Windows Programma di installazione 5.0 Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Programma di installazione 4.0 o Windows Installer 4.5 in Windows Server 2008 o Windows Vista. Windows Programma di installazione 3.0 o versioni successive in Windows Server 2003, Windows XP e Windows 2000<br/> |
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

 

 




