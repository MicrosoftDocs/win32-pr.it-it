---
description: La modalità di indirizzamento della trama del morsetto, identificata dal \_ membro del morsetto D3DTADDRESS del tipo enumerato D3DTEXTUREADDRESS, induce Direct3D a bloccare le coordinate di trama nell' \[ intervallo 0,0, 1,0 \] .
ms.assetid: 8efed38d-4c9f-4a8d-9d1b-af1c8df9292a
title: Modalità di indirizzamento della trama del morsetto (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 153ed1f044bacaec6b87420eb7df22a2557349a7
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106305189"
---
# <a name="clamp-texture-address-mode-direct3d-9"></a>Modalità di indirizzamento della trama del morsetto (Direct3D 9)

La modalità di indirizzamento della trama del morsetto, identificata dal \_ membro del morsetto D3DTADDRESS del tipo enumerato [**D3DTEXTUREADDRESS**](./d3dtextureaddress.md) , induce Direct3D a bloccare le coordinate di trama nell' \[ intervallo 0,0, 1,0 \] . Ovvero applica la trama una volta, quindi striscierà il colore dei pixel perimetrali. Si supponga, ad esempio, che l'applicazione crei una primitiva quadrata e assegna le coordinate di trama (0,0, 0,0), (0.0, 3.0), (3.0, 3.0) e (3.0, 0,0) ai vertici della primitiva. Impostando la modalità di indirizzamento della trama su D3DTADDRESS \_ Clamp, la trama viene applicata una sola volta. I colori dei pixel nella parte superiore delle colonne e la fine delle righe vengono estesi rispettivamente alla parte superiore e a destra della primitiva.

La figura seguente mostra una trama fissa.

![illustrazione di una trama e di una trama fissa](images/clamp.png)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Modalità di indirizzamento delle trame](texture-addressing-modes.md)
</dt> </dl>

 

 
