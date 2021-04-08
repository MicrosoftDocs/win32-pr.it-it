---
description: La proprietà DVDAdm. DisableScreenSaver attiva o disattiva la screen saver di sistema.
ms.assetid: 78a0512f-456a-45b6-8717-13593461a765
title: Proprietà DisableScreenSaver
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2d651026f2bf09f872655a0ef58accb3a6173dcb
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "103876034"
---
# <a name="disablescreensaver-property"></a>Proprietà DisableScreenSaver

> [!Note]  
> Questo componente è disponibile per l'uso nei sistemi operativi Microsoft Windows 2000, Windows XP e Windows Server 2003. È possibile che in versioni successive sia stata modificata o non sia più disponibile.

 

La `DVDAdm.DisableScreenSaver` proprietà attiva o disattiva la screen saver di sistema.

``` syntax
[ bDisabled = ] DVD.DVDAdm.DisableScreenSaver
```

## <a name="return-value"></a>Valore restituito

Restituisce un valore booleano che indica se le impostazioni screen saver del sistema sono disabilitate per l'applicazione DVD Player; true indica che le impostazioni sono disabilitate.

## <a name="remarks"></a>Commenti

Questa proprietà è di lettura/scrittura e il valore predefinito è true. Quando si visualizza un disco DVD-Video, un utente in genere non utilizza il mouse o la tastiera per periodi di tempo prolungati. Il controllo® ActiveX MSWebDVD Disabilita quindi il screen saver di sistema per impostazione predefinita. Oggetto

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**RestoreScreenSaver**](restorescreensaver-method.md)
</dt> <dt>

[Oggetto MSDVDAdm](msdvdadm-object.md)
</dt> </dl>

 

 



