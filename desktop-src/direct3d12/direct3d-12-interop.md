---
title: Uso di Direct3D 11, Direct3D 10 e Direct2D
description: Questa sezione illustra le tecniche di interoperabilità con le versioni precedenti di Direct3D e Direct2D, l'API Direct3D 11on12 e le linee guida per la portabilità da Direct3D 11 a Direct3D 12.
ms.assetid: 1AB98335-30B1-4244-B244-F8573524B38C
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 462febfc36c15e2af50f0d4f031bec026bbd8cd3713dafbd9678e733978f484e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118989691"
---
# <a name="working-with-direct3d-11-direct3d-10-and-direct2d"></a>Uso di Direct3D 11, Direct3D 10 e Direct2D

Questa sezione illustra le tecniche di interoperabilità con le versioni precedenti di Direct3D e Direct2D, l'API Direct3D 11on12 e le linee guida per la portabilità da Direct3D 11 a Direct3D 12.

## <a name="in-this-section"></a>Contenuto della sezione



| Argomento                                                                                             | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
|---------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Interoperabilità Direct3D 12](direct3d-12-with-direct3d-11--direct-2d-and-gdi.md)<br/>             | D3D12 può essere usato per scrivere applicazioni in componenti. <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| [D3D11On12](direct3d-11-on-12.md)<br/>                                             | D3D11On12 è un meccanismo tramite il quale gli sviluppatori possono usare interfacce e oggetti D3D11 per l'API D3D12. D3D11on12 consente ai componenti scritti con D3D11 (ad esempio, testo D2D e interfaccia utente) di funzionare insieme ai componenti scritti per l'API D3D12. D3D11on12 consente anche la portabilità incrementale di un'applicazione da D3D11 a D3D12, consentendo a parti dell'app di continuare a usare D3D11 come destinazione per semplicità, mentre altre hanno come destinazione D3D12 per le prestazioni, pur avendo sempre un rendering completo e corretto. D3D11On12 semplifica l'uso delle tecniche di interoperabilità per condividere le risorse e sincronizzare il lavoro tra le due API. <br/> |
| [Conversione da Direct3D 11 a Direct3D 12](porting-from-direct3d-11-to-direct3d-12.md)<br/> | Questa sezione fornisce alcune indicazioni sulla portabilità da un motore di grafica Direct3D 11 personalizzato a Direct3D 12.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Guida per programmatori Direct3D 12](directx-12-programming-guide.md)
</dt> </dl>

 

 





