---
description: Clonazione e condivisione (Direct3D 9)
ms.assetid: 1dabe611-bf3b-49bf-99ab-dbdfd343f885
title: Clonazione e condivisione (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 983e674af4cdd24e21fcc2517eb8a32d6aec291c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103878274"
---
# <a name="cloning-and-sharing-direct3d-9"></a>Clonazione e condivisione (Direct3D 9)

## <a name="cloning-parameters"></a>Parametri di clonazione

La clonazione presenta le restrizioni seguenti.

-   I cloni ereditano il pool dell'effetto originale. Vedere la sezione relativa ai parametri di condivisione.
-   I cloni ereditano le tecniche, le sessioni, i parametri e le annotazioni dell'effetto originale (incluse tutte le annotazioni aggiunte con [**ID3DXEffect**](id3dxeffect.md)).
-   I cloni ereditano le annotazioni aggiunte dinamicamente dall'effetto originale.
-   La clonazione su un nuovo dispositivo non riuscirà se il pool dell'effetto originale non era **null** e l'effetto originale conteneva un parametro condiviso dipendente dal dispositivo, ad esempio una trama o uno shader.

## <a name="sharing-parameters"></a>Condivisione di parametri

Un pool è un buffer che condivide parametri di effetto tra diversi effetti. Per aggiungere parametri a un pool, specificare un utilizzo condiviso quando viene creato l'effetto.

Un pool presenta le restrizioni seguenti.

-   Un parametro viene aggiunto al pool la prima volta che un effetto contenente il parametro (condiviso) viene aggiunto al pool.
-   Un pool ottiene i valori iniziali dal primo parametro condiviso. i parametri condivisi successivamente ottengono i valori dal pool.
-   Un parametro viene eliminato dal pool quando vengono rilasciati tutti i riferimenti di effetto al parametro condiviso.
-   Tutti gli effetti nel pool che contengono lo stesso parametro (Shared) dipendente dal dispositivo devono avere lo stesso dispositivo.

È possibile utilizzare **null** per specificare nessun pool, nel qual caso non viene condiviso alcun parametro. Questa operazione è quasi equivalente alla specifica di un pool univoco solo per questo effetto. L'unica differenza è che quando l'effetto viene clonato, il clone non condividerà i parametri condivisi con quello originale.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Formato effetto](dx9-graphics-reference-effects-file-format.md)
</dt> </dl>

 

 



