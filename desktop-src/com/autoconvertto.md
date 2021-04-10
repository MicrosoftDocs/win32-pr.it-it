---
title: AutoConvertTo
description: Specifica la conversione automatica di una determinata classe di oggetti in una nuova classe di oggetti.
ms.assetid: e34b799b-0d23-4034-ba79-49e92ec4dea7
keywords:
- AutoConvertTo chiave del registro di sistema COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 160f6591ed318ad7622e0bf3c0af5187f95d3be3
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103855185"
---
# <a name="autoconvertto"></a>AutoConvertTo

Specifica la conversione automatica di una determinata classe di oggetti in una nuova classe di oggetti.

## <a name="registry-entry"></a>Voce del Registro di sistema

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\CLSID
   {CLSID}
      AutoConvertTo = value
```

## <a name="remarks"></a>Commenti

Si tratta di un valore **reg \_ SZ** che specifica l'identificatore di classe dell'oggetto in cui deve essere convertito l'oggetto o la classe di oggetti specificata.

Questa chiave viene in genere utilizzata per convertire automaticamente i file creati da una versione precedente di un'applicazione in una versione più recente dell'applicazione.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**OleDoAutoConvert**](/windows/desktop/api/Ole2/nf-ole2-oledoautoconvert)
</dt> <dt>

[**OleGetAutoConvert**](/windows/desktop/api/Ole2/nf-ole2-olegetautoconvert)
</dt> <dt>

[**OleSetAutoConvert**](/windows/desktop/api/Ole2/nf-ole2-olesetautoconvert)
</dt> </dl>

 

 




