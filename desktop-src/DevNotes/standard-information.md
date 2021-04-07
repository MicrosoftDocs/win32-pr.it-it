---
description: Contiene l'attributo di informazioni standard. Questo attributo è presente in ogni record di file di base e deve essere residente.
ms.assetid: 8e668309-2722-4115-923d-bf0aa78d24f1
title: Struttura STANDARD_INFORMATION
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- STANDARD_INFORMATION
api_type:
- NA
api_location: ''
ms.openlocfilehash: 4927553ac593475f8659932468227362ae19fe59
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104049077"
---
# <a name="standard_information-structure"></a>\_Struttura delle informazioni standard

\[Questa struttura è valida solo per la versione 3 dei volumi NTFS. potrebbe essere modificato nelle versioni future.\]

Contiene l'attributo di informazioni standard. Questo attributo è presente in ogni record di file di base e deve essere residente.

## <a name="syntax"></a>Sintassi


```C++
typedef struct _STANDARD_INFORMATION {
  UCHAR Reserved[0x30];
  ULONG OwnerId;
  ULONG SecurityId;
} STANDARD_INFORMATION, *PSTANDARD_INFORMATION;
```



## <a name="members"></a>Members

<dl> <dt>

**Reserved**
</dt> <dd>

Riservato.

</dd> <dt>

**OwnerId**
</dt> <dd>

Identificatore del proprietario del file, dall'indice di sicurezza.

</dd> <dt>

**SecurityId**
</dt> <dd>

Identificatore di sicurezza per il file.

</dd> </dl>

## <a name="remarks"></a>Commenti

Si noti che non è presente alcun file di intestazione associato per questa struttura.

Questa definizione di struttura è valida solo per la versione principale 3 e secondaria 0 o 1, come indicato [**da \_ FSCTL \_ ottenere \_ \_ i dati del volume NTFS**](/windows/win32/api/winioctl/ni-winioctl-fsctl_get_ntfs_volume_data).

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Tabella file master](master-file-table.md)
</dt> </dl>

 

 
