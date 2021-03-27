---
title: Uso del collegamento shader
description: Viene illustrato come creare funzioni HLSL precompilate, assemblarle in librerie e collegarle in shader completi in fase di esecuzione.
ms.assetid: 3A1597FF-F848-415E-BDF8-199C69C05C3B
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d7528415f1bedb0364a9c4b09126a983222fc42b
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "103729914"
---
# <a name="using-shader-linking"></a>Uso del collegamento shader

Viene illustrato come creare funzioni HLSL precompilate, assemblarle in librerie e collegarle in shader completi in fase di esecuzione. Il collegamento dello shader è supportato a partire da Windows 8.1.

**Obiettivo:** Informazioni su come usare il collegamento dello shader.

## <a name="prerequisites"></a>Prerequisiti

Partiamo dal presupposto che tu abbia familiarità con C++. Devi inoltre avere un'esperienza di base dei concetti di programmazione di grafica.

**Tempo totale per il completamento:** 60 minuti.

## <a name="where-to-go-from-here"></a>Dove proseguire

Vedere anche [API del compilatore HLSL](dx-graphics-d3dcompiler-reference.md).

Ti mostreremo come:

-   Compilare il codice dello shader
-   Caricare il codice compilato in una libreria shader
-   Associare le risorse dagli slot di origine agli slot di destinazione
-   Costrutto Function-linking-graphs (FLGs) per gli shader
-   Collegare i grafici shader con una libreria shader per produrre un BLOB dello shader che può essere usato dal runtime Direct3D

Successivamente, si crea una libreria shader e si associano le risorse da slot di origine a slot di destinazione.

[Creazione del pacchetto di una libreria shader](pachaging-a-shader-library.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Guida alla programmazione per HLSL](dx-graphics-hlsl-pguide.md)
</dt> <dt>

[Grafica Direct3D 11](/windows/desktop/direct3d11/atoc-dx-graphics-direct3d-11)
</dt> <dt>

[DXGI](/windows/desktop/direct3ddxgi/dx-graphics-dxgi)
</dt> </dl>

 

 