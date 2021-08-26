---
title: AutoConvertTo
description: Specifica la conversione automatica di una determinata classe di oggetti in una nuova classe di oggetti .
ms.assetid: e34b799b-0d23-4034-ba79-49e92ec4dea7
keywords:
- Com della chiave del Registro di sistema AutoConvertTo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d5ea2b32445bb7107dcbfdc2aec8aee518fdd474674e76fdbd820265d06b6160
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120097051"
---
# <a name="autoconvertto"></a>AutoConvertTo

Specifica la conversione automatica di una determinata classe di oggetti in una nuova classe di oggetti .

## <a name="registry-entry"></a>Voce del Registro di sistema

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\CLSID
   {CLSID}
      AutoConvertTo = value
```

## <a name="remarks"></a>Commenti

Si tratta di **un \_ valore REG SZ** che specifica l'identificatore di classe dell'oggetto in cui deve essere convertito l'oggetto o la classe di oggetti specificata.

Questa chiave viene in genere usata per convertire automaticamente i file creati da una versione precedente di un'applicazione in una versione più recente dell'applicazione.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**OleDoAutoConvert**](/windows/desktop/api/Ole2/nf-ole2-oledoautoconvert)
</dt> <dt>

[**OleGetAutoConvert**](/windows/desktop/api/Ole2/nf-ole2-olegetautoconvert)
</dt> <dt>

[**OleSetAutoConvert**](/windows/desktop/api/Ole2/nf-ole2-olesetautoconvert)
</dt> </dl>

 

 




