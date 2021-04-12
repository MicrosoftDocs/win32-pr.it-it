---
description: In questa sezione vengono elencati i problemi che possono verificarsi quando si utilizza Direct3D 9 su driver scritti per versioni di Direct3D precedenti a Direct3D 9.
ms.assetid: 891198e8-6c45-4f03-99bb-e24a4082b0d8
title: Utilizzo di driver precedenti (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 76567bc4778924835e20a476b03dc94ea77739fd
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104401105"
---
# <a name="working-with-earlier-drivers-direct3d-9"></a>Utilizzo di driver precedenti (Direct3D 9)

In questa sezione vengono elencati i problemi che possono verificarsi quando si utilizza Direct3D 9 su driver scritti per versioni di Direct3D precedenti a Direct3D 9.

-   Quando si usa un dispositivo T&L HAL, l'intensità della nebbia viene calcolata, ma l'operazione di valore assoluto non viene applicata a questo valore. Il valore viene invece lasciato negativo se corrisponde a quello calcolato. Il modo migliore per evitare questa situazione consiste nell'impostare le trasformazioni in modo appropriato. Un metodo meno consigliato consiste nel fare in modo che i valori di inizio e di nebbia negativi corrispondano.

Per verificare la presenza di un driver Direct3D 9, cercare un valore diverso da zero per D3DDEVCAPS2 \_ STREAMOFFSET nel membro DevCaps2 di [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Suggerimenti per la programmazione](programming-tips.md)
</dt> </dl>

 

 



