---
description: Questa sezione elenca i problemi che possono verificarsi quando si lavora con Direct3D 9 su driver scritti per versioni di Direct3D precedenti a Direct3D 9.
ms.assetid: 891198e8-6c45-4f03-99bb-e24a4082b0d8
title: Uso di driver precedenti (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 24284c706d49ce3294e23486f72150ffd74ee376e2be0d7d06dca09877eb7cc8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118796910"
---
# <a name="working-with-earlier-drivers-direct3d-9"></a>Uso di driver precedenti (Direct3D 9)

Questa sezione elenca i problemi che possono verificarsi quando si lavora con Direct3D 9 su driver scritti per versioni di Direct3D precedenti a Direct3D 9.

-   Quando si lavora con un dispositivo T&L HAL, viene calcolata l'intensità della festosa, ma l'operazione sul valore assoluto non viene applicata a questo valore. Al contrario, il valore viene lasciato negativo se questo è ciò che viene calcolato. Il modo migliore per evitare questa situazione è configurare le trasformazioni in modo appropriato. Un metodo meno consigliato è rendere i valori di inizio e fine della nebbia negativi in modo che corrispondano.

Per verificare la presenza di un driver Direct3D 9, cercare un valore diverso da zero per D3DDEVCAPS2 STREAMOFFSET nel membro \_ DevCaps2 di [**D3DCAPS9.**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Programmazione Suggerimenti](programming-tips.md)
</dt> </dl>

 

 



