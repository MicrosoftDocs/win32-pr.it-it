---
title: Uso di Direct3D 11, Direct3D 10 e Direct2D
description: Questa sezione illustra le tecniche di interoperabilità con le versioni precedenti di Direct3D e Direct2D, l'API Direct3D 11on12 e le linee guida per il porting da Direct3D 11 a Direct3D 12.
ms.assetid: 1AB98335-30B1-4244-B244-F8573524B38C
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b200da0708b9b990b102a77867669217318f1d67
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "74103725"
---
# <a name="working-with-direct3d-11-direct3d-10-and-direct2d"></a>Uso di Direct3D 11, Direct3D 10 e Direct2D

Questa sezione illustra le tecniche di interoperabilità con le versioni precedenti di Direct3D e Direct2D, l'API Direct3D 11on12 e le linee guida per il porting da Direct3D 11 a Direct3D 12.

## <a name="in-this-section"></a>Contenuto della sezione



| Argomento                                                                                             | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
|---------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Interoperabilità di Direct3D 12](direct3d-12-with-direct3d-11--direct-2d-and-gdi.md)<br/>             | D3D12 può essere usato per scrivere applicazioni con componenti. <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| [D3D11On12](direct3d-11-on-12.md)<br/>                                             | D3D11On12 è un meccanismo mediante il quale gli sviluppatori possono usare le interfacce e gli oggetti di D3D11 per guidare l'API D3D12. D3D11on12 consente ai componenti scritti con D3D11, ad esempio D2D testo e interfaccia utente, di interagire con i componenti scritti per l'API D3D12. D3D11on12 consente anche il porting incrementale di un'applicazione da D3D11 a D3D12, consentendo a parti dell'app di continuare a usare D3D11 per semplicità, mentre altre sono destinate a D3D12 per le prestazioni, pur avendo sempre il rendering completo e corretto. D3D11On12 rende più semplice l'uso di tecniche di interoperabilità per condividere le risorse e sincronizzare il lavoro tra le due API. <br/> |
| [Conversione da Direct3D 11 a Direct3D 12](porting-from-direct3d-11-to-direct3d-12.md)<br/> | In questa sezione vengono fornite alcune indicazioni sul porting da un motore di grafica Direct3D 11 personalizzato a Direct3D 12.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Guida per programmatori Direct3D 12](directx-12-programming-guide.md)
</dt> </dl>

 

 





