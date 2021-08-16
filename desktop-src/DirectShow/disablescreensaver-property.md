---
description: La proprietà DVDAdm.DisableScreenSaver attiva o screen saver sistema.
ms.assetid: 78a0512f-456a-45b6-8717-13593461a765
title: Proprietà DisableScreenSaver
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9bc714dbbdc3e9b144f2d49cb54871cdf09baad5df39f8e18b962d7fc415d44a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117821129"
---
# <a name="disablescreensaver-property"></a>Proprietà DisableScreenSaver

> [!Note]  
> Questo componente è disponibile per l'uso nei sistemi operativi Microsoft Windows 2000, Windows XP e Windows Server 2003. È possibile che in versioni successive sia stata modificata o non sia più disponibile.

 

La `DVDAdm.DisableScreenSaver` proprietà attiva o disattiva screen saver sistema.

``` syntax
[ bDisabled = ] DVD.DVDAdm.DisableScreenSaver
```

## <a name="return-value"></a>Valore restituito

Restituisce un valore booleano che indica se le impostazioni screen saver del sistema sono disabilitate per l'applicazione lettore DVD. true indica che le impostazioni sono disabilitate.

## <a name="remarks"></a>Commenti

Questa proprietà è di lettura/scrittura con il valore predefinito true. Quando si visualizza un DVD-Video, un utente in genere non usa il mouse o la tastiera per lunghi periodi di tempo. Il controllo ActiveX® MSWebDVD disabilita quindi l'screen saver di sistema per impostazione predefinita. Oggetto

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**RestoreScreenSaver**](restorescreensaver-method.md)
</dt> <dt>

[Oggetto MSDVDAdm](msdvdadm-object.md)
</dt> </dl>

 

 



