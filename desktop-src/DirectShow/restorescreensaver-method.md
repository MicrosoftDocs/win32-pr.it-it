---
description: Il metodo DVDAdm. RestoreScreenSaver Ripristina le impostazioni di screen saver di sistema.
ms.assetid: 606ab850-95bf-4c60-b7cf-e3a94ceee7a7
title: Metodo RestoreScreenSaver
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 85b747aa21815bb37cc7db2296347c9890a06914
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "106303911"
---
# <a name="restorescreensaver-method"></a>Metodo RestoreScreenSaver

> [!Note]  
> Questo componente è disponibile per l'uso nei sistemi operativi Microsoft Windows 2000, Windows XP e Windows Server 2003. È possibile che in versioni successive sia stata modificata o non sia più disponibile.

 

Il `DVDAdm.RestoreScreenSaver` metodo ripristina le impostazioni del screen saver di sistema.

``` syntax
DVD.DVDAdm.RestoreScreenSaver()
```

## <a name="return-value"></a>Valore restituito

Nessun valore restituito.

## <a name="remarks"></a>Commenti

In genere, un'applicazione DVD Disabilita la screen saver di sistema all'avvio impostando la proprietà [**DisableScreenSaver**](disablescreensaver-property.md) su true e riabilitando nuovamente l'screen saver quando l'applicazione DVD viene chiusa chiamando `RestoreScreenSaver` . Se un'applicazione non utilizza le impostazioni screen saver del sistema, non è necessario chiamare questo metodo o impostare la proprietà **DisableScreenSaver** .

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Oggetto MSDVDAdm](msdvdadm-object.md)
</dt> </dl>

 

 



