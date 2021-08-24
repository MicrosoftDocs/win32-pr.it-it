---
title: Uso del collegamento di shader
description: Viene illustrato come creare funzioni HLSL precompilate, crearne il pacchetto in librerie e collegarle a shader completi in fase di esecuzione.
ms.assetid: 3A1597FF-F848-415E-BDF8-199C69C05C3B
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e44f382596f3839460943fdbefe5687c4e7b18401db016ad3f834284e994217b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119742281"
---
# <a name="using-shader-linking"></a>Uso del collegamento di shader

Viene illustrato come creare funzioni HLSL precompilate, crearne il pacchetto in librerie e collegarle a shader completi in fase di esecuzione. Il collegamento dello shader è supportato a partire da Windows 8.1.

**Obiettivo:** Informazioni su come usare il collegamento dello shader.

## <a name="prerequisites"></a>Prerequisiti

Partiamo dal presupposto che tu abbia familiarità con C++. Devi inoltre avere un'esperienza di base dei concetti di programmazione di grafica.

**Tempo totale per il completamento:** 60 minuti.

## <a name="where-to-go-from-here"></a>Dove proseguire

Vedere anche [API del compilatore HLSL.](dx-graphics-d3dcompiler-reference.md)

Ti mostreremo come:

-   Compilare il codice dello shader
-   Caricare il codice compilato in una libreria shader
-   Associare le risorse dagli slot di origine agli slot di destinazione
-   Costruire grafici di collegamento delle funzioni (FFLG) per shader
-   Collegare i grafici shader a una libreria shader per produrre un BLOB shader che il runtime Direct3D può usare

Successivamente si crea una libreria shader e si associano le risorse dagli slot di origine agli slot di destinazione.

[Creazione del pacchetto di una libreria shader](pachaging-a-shader-library.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Guida alla programmazione per HLSL](dx-graphics-hlsl-pguide.md)
</dt> <dt>

[Grafica Direct3D 11](/windows/desktop/direct3d11/atoc-dx-graphics-direct3d-11)
</dt> <dt>

[DXGI](/windows/desktop/direct3ddxgi/dx-graphics-dxgi)
</dt> </dl>

 

 