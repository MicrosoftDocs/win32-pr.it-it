---
description: Il metodo FileHash dell'oggetto Installer accetta il percorso di un file e restituisce un hash a 128 bit del file. Le informazioni sull'hash del file vengono restituite come oggetto Record. L'intero hash del file a 128 bit viene restituito come quattro campi della proprietà IntegerData a 32 bit.
ms.assetid: 065ffde1-4d7c-4e71-9315-7926d4cd38ed
title: Metodo Installer.FileHash
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.FileHash
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: a2da76ef3f0606002e26e8c320f83ca45e46bbbeb573d509c235c9fca8932247
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118630792"
---
# <a name="installerfilehash-method"></a>Metodo Installer.FileHash

Il **metodo FileHash** dell'oggetto [**Installer**](installer-object.md) accetta il percorso di un file e restituisce un hash a 128 bit del file. Le informazioni sull'hash del file vengono restituite come [**oggetto Record.**](record-object.md) L'intero hash del file a 128 bit viene restituito come quattro campi della proprietà [**IntegerData**](record-integerdata.md) a 32 bit.

I valori restituiti [**nell'oggetto Record**](record-object.md) corrispondono ai quattro campi della struttura [**MSIFILEHASHINFO**](/windows/desktop/api/Msi/ns-msi-msifilehashinfo) restituiti [**da MsiGetFileHash.**](/windows/desktop/api/Msi/nf-msi-msigetfilehasha) La numerazione di quattro campi è in base 1 nella [tabella MsiFileHash](msifilehash-table.md).

-   Il campo 1 corrisponde alla colonna HashPart1.
-   Il campo 2 corrisponde alla colonna HashPart2.
-   Il campo 3 corrisponde alla colonna HashPart3.
-   Il campo 4 corrisponde alla colonna HashPart4.

## <a name="syntax"></a>Sintassi


```JScript
Installer.FileHash(
  FilePath,
  Options
)
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Filepath* 
</dt> <dd>

Percorso del file di cui eseguire l'hashing.

</dd> <dt>

*Opzioni* 
</dt> <dd>

Riservato per utilizzi futuri.

Il valore di questo parametro deve essere 0 (zero).

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se ha esito positivo, questo metodo restituisce [**un oggetto Record**](record-object.md) che contiene l'hash del file.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versione<br/> | Windows Programma di installazione 5.0 Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Installer 4.0 o Windows Installer 4.5 in Windows Server 2008 o Windows Vista. Windows Programma di installazione Windows Server 2003 o Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ IInstaller è definito come 000C1090-0000-0000-C000-000000000046<br/>                                                                                                                                                                           |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Controllo delle versioni dei file predefinito](default-file-versioning.md)
</dt> <dt>

[Gestire le dimensioni e le versioni dei file](manage-file-sizes-and-versions.md)
</dt> <dt>

[Tabella MsiFileHash](msifilehash-table.md)
</dt> <dt>

[**MsiGetFileHash**](/windows/desktop/api/Msi/nf-msi-msigetfilehasha)
</dt> </dl>

 

 




