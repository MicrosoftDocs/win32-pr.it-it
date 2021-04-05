---
title: Voce del registro di sistema runtime
description: Voce del registro di sistema runtime
ms.assetid: 3b2880f9-acb9-4a13-8364-67fbe76f8d29
keywords:
- Windows Media Player, voci del registro di sistema di runtime
- Windows Media Player, estensioni di file
- Windows Media Player, registro di sistema
- Registro di sistema, estensioni di file
- Registro di sistema, voci di runtime
- Registro di sistema, impostazioni per Windows Media Player
- impostazioni del registro di sistema estensione del nome file
- voci del registro di sistema di runtime
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b01a83c3642f49a9fdbe7f8c51f157a154a9843b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104044959"
---
# <a name="runtime-registry-entry"></a>Voce del registro di sistema runtime

Quando Windows Media Player rileva un'estensione del nome di file personalizzata, Cerca una sottochiave del registro di sistema corrispondente all'estensione. La sottochiave è descritta in [impostazioni del registro di sistema estensione del nome file](file-name-extension-registry-settings.md). Una delle voci del registro di sistema che possono essere visualizzate sotto la sottochiave dell'estensione è la voce di **Runtime** .

La voce **Runtime** specifica la tecnologia sottostante che Windows Media Player può utilizzare per riprodurre o convertire file multimediali digitali con estensione personalizzata. La voce **Runtime** ha il formato seguente.



|          |                |                                                               |
|----------|----------------|---------------------------------------------------------------|
| **Nome** | **Tipo**       | **Valore**                                                     |
| Runtime  | **REG \_ DWORD** | Numero intero positivo che identifica la tecnologia sottostante. |



 

Il valore della voce di **Runtime** deve essere uno dei seguenti.



| **Valore (decimale)** | **Descrizione**                                                                            |
|---------------------|--------------------------------------------------------------------------------------------|
| 6                   | Eseguire il rendering usando Windows Media Format SDK.                                                 |
| 7                   | Eseguire il rendering con Microsoft DirectShow.                                                         |
| 13                  | Converte il file utilizzando il plug-in di conversione specificato. Richiede Windows Media Player 11. |



 

I valori 6 e 7 della voce del registro di sistema di **Runtime** sono supportati dalla serie Windows Media Player 9 e versioni successive. Il valore 13 è supportato da Windows Media Player 11.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Sottochiave ConvertPluginCLSID**](convertpluginclsid-subkey.md)
</dt> <dt>

[**Impostazioni del registro di sistema estensione del nome file**](file-name-extension-registry-settings.md)
</dt> </dl>

 

 




