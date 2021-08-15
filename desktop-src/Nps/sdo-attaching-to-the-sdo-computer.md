---
title: Collegamento al computer SDO
description: Con il puntatore di interfaccia restituito da CoCreateInstance, chiamare il metodo ISdoMachine Attach.
ms.assetid: b28691ef-4054-4cd1-92aa-72ad9902fba3
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5863302da3f213c1360c254782a31c0dfc4fcb9a946f5827155862bca01405cb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118362189"
---
# <a name="attaching-to-the-sdo-computer"></a>Collegamento al computer SDO

Con il puntatore di interfaccia restituito da [**CoCreateInstance,**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance)chiamare il [**metodo ISdoMachine::Attach.**](/windows/desktop/api/sdoias/nf-sdoias-isdomachine-attach) Passare **NULL** come parametro al **metodo Attach.** Il valore **NULL** specifica che **Attach** associa l'oggetto computer al computer locale. Il collegamento a un computer remoto non è supportato.

Per determinare se il computer locale è già collegato, chiamare il [**metodo ISdoMachine::GetAttachedComputer.**](/windows/desktop/api/sdoias/nf-sdoias-isdomachine-getattachedcomputer)

Vedere [Collegamento a un computer SDO-Enabled per](/windows/desktop/Nps/sdo-attaching-to-an-sdo-enabled-computer) il codice di esempio che illustra come connettersi al computer locale.

 

 