---
description: Clonazione e condivisione (Direct3D 9)
ms.assetid: 1dabe611-bf3b-49bf-99ab-dbdfd343f885
title: Clonazione e condivisione (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 96add856c6e3c675cbf3ac225d39517214ed9dc002abded6f4f7f9f75d4736bc
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119857701"
---
# <a name="cloning-and-sharing-direct3d-9"></a>Clonazione e condivisione (Direct3D 9)

## <a name="cloning-parameters"></a>Parametri di clonazione

La clonazione presenta le restrizioni seguenti.

-   I cloni ereditano il pool dell'effetto originale. Vedere la sezione Parametri di condivisione.
-   I cloni ereditano le tecniche, i passaggi, i parametri e le annotazioni dell'effetto originale (incluse tutte le annotazioni aggiunte con [**ID3DXEffect).**](id3dxeffect.md)
-   I cloni ereditano le annotazioni aggiunte dinamicamente dell'effetto originale.
-   La clonazione in un nuovo dispositivo avrà esito negativo se il pool dell'effetto originale non è **NULL** e l'effetto originale contiene un parametro dipendente dal dispositivo condiviso, ad esempio una trama o uno shader.

## <a name="sharing-parameters"></a>Condivisione dei parametri

Un pool è un buffer che condivide i parametri di effetto tra diversi effetti. Per aggiungere parametri a un pool, specificare un utilizzo condiviso quando viene creato l'effetto.

Un pool presenta le restrizioni seguenti.

-   Un parametro viene aggiunto al pool la prima volta che un effetto contenente tale parametro (condiviso) viene aggiunto al pool.
-   Un pool ottiene i valori iniziali dal primo parametro condiviso. I parametri condivisi successivamente ottengono i relativi valori dal pool.
-   Un parametro viene eliminato dal pool quando vengono rilasciati tutti i riferimenti di effetto al parametro condiviso.
-   Tutti gli effetti nel pool che contengono lo stesso parametro dipendente dal dispositivo (condiviso) devono avere lo stesso dispositivo.

**È** possibile usare NULL per non specificare alcun pool, nel qual caso non viene condiviso alcun parametro. Ciò equivale quasi a specificare un pool univoco solo per questo effetto. La singola differenza è che quando l'effetto viene clonato, il clone non condividerà i parametri condivisi con l'originale.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Formato effetto](dx9-graphics-reference-effects-file-format.md)
</dt> </dl>

 

 



