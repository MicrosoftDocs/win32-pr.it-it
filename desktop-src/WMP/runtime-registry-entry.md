---
title: Voce del Registro di sistema di runtime
description: Voce del Registro di sistema di runtime
ms.assetid: 3b2880f9-acb9-4a13-8364-67fbe76f8d29
keywords:
- Windows Media Player,voci del Registro di sistema di runtime
- Windows Media Player,estensioni di file
- Windows Media Player,registro
- registro, estensioni di file
- registro, voci di runtime
- registro, impostazioni per Windows Media Player
- Impostazioni del Registro di sistema dell'estensione di file
- voci del Registro di sistema di runtime
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3bf485038965184add320e49c29482672c770f48
ms.sourcegitcommit: 0f7a8198bacd5493ab1e78a9583c7a3578794765
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 05/25/2021
ms.locfileid: "110424110"
---
# <a name="runtime-registry-entry"></a>Voce del Registro di sistema di runtime

Quando Windows Media Player rileva un'estensione di file personalizzata, cerca una sottochiave del Registro di sistema corrispondente all'estensione. La sottochiave è descritta in Impostazioni del Registro di [sistema dell'estensione file](file-name-extension-registry-settings.md). Una delle voci del Registro di sistema che possono essere visualizzate sotto la sottochiave dell'estensione è la **voce Runtime.**

La **voce Runtime** specifica la tecnologia sottostante che Windows Media Player possibile usare per riprodurre o convertire file multimediali digitali con estensione personalizzata. La **voce Runtime** ha il formato seguente.



|   Nome   |   Type         |   valore                                                       |
|----------|----------------|---------------------------------------------------------------|
| Runtime  | **REG \_ DWORD** | Intero positivo che identifica la tecnologia sottostante. |



 

Il valore della voce **Runtime** deve essere uno dei seguenti.



| **Valore (decimale)** | **Descrizione**                                                                            |
|---------------------|--------------------------------------------------------------------------------------------|
| 6                   | Eseguire il rendering con Windows Media Format SDK.                                                 |
| 7                   | Eseguire il rendering con Microsoft DirectShow.                                                         |
| 13                  | Convertire il file usando il plug-in di conversione specificato. Richiede Windows Media Player 11. |



 

I **valori 6** e 7 della voce del Registro di sistema Runtime sono supportati Windows Media Player serie 9 e successive. Il valore 13 è supportato da Windows Media Player 11.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Sottochiave ConvertPluginCLSID**](convertpluginclsid-subkey.md)
</dt> <dt>

[**Impostazioni del Registro di sistema dell'estensione del nome file**](file-name-extension-registry-settings.md)
</dt> </dl>

 

 




