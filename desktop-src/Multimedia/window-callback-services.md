---
title: Servizi di callback della finestra
description: Servizi di callback della finestra
ms.assetid: 227602e5-7ea1-4afd-ac88-cfeabe746d1f
keywords:
- audio multimediale, servizi di callback della finestra
- audio, servizi di callback della finestra
- mixer audio, servizi di callback della finestra
- mixer, servizi di callback delle finestre
- servizi di callback della finestra
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0248928d339dc6c1737ee9dc47f72bac0fb42fe76774e6062177c29064b44257
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119781411"
---
# <a name="window-callback-services"></a>Servizi di callback della finestra

I servizi mixer forniscono servizi di callback della finestra in modo che l'applicazione possa elaborare i messaggi dai driver del mixer. Per usare questi servizi, specificare il flag CALLBACK WINDOW nel parametro fdwOpen e un handle di finestra nel \_ *parametro dwCallback* della [**funzione mixerOpen.**](/windows/win32/api/mmeapi/nf-mmeapi-mixeropen)  I messaggi del driver vengono inviati alla funzione della routine della finestra per la finestra identificata dall'handle in *dwCallback*. I messaggi sono specifici del tipo di dispositivo audio.

 

 