---
description: Il metodo DVDAdm.RestoreScreenSaver ripristina le impostazioni screen saver sistema.
ms.assetid: 606ab850-95bf-4c60-b7cf-e3a94ceee7a7
title: Metodo RestoreScreenSaver
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 684250b237105e391472237a5e7093855dd82ef5b59ffbbaa20ebecf386da302
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119696971"
---
# <a name="restorescreensaver-method"></a>Metodo RestoreScreenSaver

> [!Note]  
> Questo componente è disponibile per l'uso nei sistemi operativi Microsoft Windows 2000, Windows XP e Windows Server 2003. È possibile che in versioni successive sia stata modificata o non sia più disponibile.

 

Il `DVDAdm.RestoreScreenSaver` metodo ripristina le impostazioni screen saver sistema.

``` syntax
DVD.DVDAdm.RestoreScreenSaver()
```

## <a name="return-value"></a>Valore restituito

Nessun valore restituito.

## <a name="remarks"></a>Commenti

In genere, un'applicazione DVD disabilita il screen saver del sistema all'avvio impostando la proprietà [**DisableScreenSaver**](disablescreensaver-property.md) su true e quindi riattiva il screen saver quando l'applicazione DVD viene chiusa chiamando `RestoreScreenSaver` . Se un'applicazione non usa le impostazioni screen saver sistema, non deve chiamare questo metodo o impostare la **proprietà DisableScreenSaver.**

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Oggetto MSDVDAdm](msdvdadm-object.md)
</dt> </dl>

 

 



