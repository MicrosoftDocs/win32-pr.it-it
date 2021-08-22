---
title: Risorsa BITMAP
description: Definisce una bitmap utilizzata da un'applicazione nella relativa visualizzazione sullo schermo o come elemento in un menu o in un controllo.
ms.assetid: 2db2f7f0-735f-4aac-9813-c04a2f7788b2
keywords:
- Menu delle risorse BITMAP e altre risorse
topic_type:
- apiref
api_name:
- BITMAP
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ff75f235e8aa1787e93f9420b4d7ed27f440cdc09510547295ebced4ec494bdd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118734899"
---
# <a name="bitmap-resource"></a>Risorsa BITMAP

Definisce una bitmap utilizzata da un'applicazione nella relativa visualizzazione sullo schermo o come elemento in un menu o in un controllo.

``` syntax
nameID BITMAP filename
```

## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="nameID"></span><span id="nameid"></span><span id="NAMEID"></span>*Nameid*
</dt> <dd>

Nome univoco o valore intero senza segno a 16 bit che identifica la risorsa.

</dd> <dt>

<span id="filename"></span><span id="FILENAME"></span>*Filename*
</dt> <dd>

Nome del file che contiene la risorsa. Il nome deve essere un nome di file valido. deve essere un percorso completo se il file non si trova nella directory di lavoro corrente. Il percorso deve essere una stringa tra virgolette.

</dd> </dl>

Alcuni attributi sono supportati anche per la compatibilità con le versioni precedenti. Per altre informazioni, vedere [Attributi comuni delle risorse](common-resource-attributes.md).

## <a name="examples"></a>Esempio

L'esempio seguente definisce due risorse bitmap:

``` syntax
disk1   BITMAP "disk.bmp"
12      BITMAP "diskette.bmp"
```

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Uso delle bitmap](/windows/desktop/gdi/using-bitmaps)
</dt> <dt>

[**LoadBitmap**](/windows/desktop/api/winuser/nf-winuser-loadbitmapa)
</dt> <dt>

[**Loadimage**](/windows/desktop/api/Winuser/nf-winuser-loadimagea)
</dt> </dl>

 

 