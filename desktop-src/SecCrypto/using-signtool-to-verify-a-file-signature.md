---
description: Illustra come usare SignTool per verificare la firma di un file.
ms.assetid: 9c40a397-19ea-4600-97ee-987dd10f4ef8
title: Uso di SignTool per verificare la firma di un file
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 85e91df7a64a8db48d04ceba9df5fbc3fd358058
ms.sourcegitcommit: 7024106e3420607420bb04c3f88d9bb4827038c8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/25/2021
ms.locfileid: "107954924"
---
# <a name="using-signtool-to-verify-a-file-signature"></a>Uso di SignTool per verificare la firma di un file

Il comando seguente verifica la firma di un file *denominatoMyControl.exe*:

**Verifica signTool** *MyControl.exe*

Se l'esempio precedente ha esito negativo, la firma potrebbe usare un certificato di firma del codice. [Per impostazione predefinita, SignTool](signtool.md) fa riferimento ai criteri del driver Windows per la verifica.

Il comando seguente verifica la firma usando i criteri di verifica dell'autenticazione predefiniti:

**SignTool verify /pa** *MyControl.exe*

Il comando seguente verifica un file di sistema che può essere firmato in un catalogo:

**Verifica SignTool /a** *SysFile.dll*

Il comando seguente verifica un file di sistema firmato in un catalogo denominato *MyCat.cat*:

**SignTool verify /c** *MyCat.cat* *MyFile.ini*

Per qualsiasi [verifica SignTool,](signtool.md) è possibile recuperare il firmatario del certificato. Il comando seguente verifica un file di sistema e visualizza il certificato del firmatario:

**SignTool verify /v** *MyControl.exe*

[SignTool](signtool.md) restituisce il testo della riga di comando che indica il risultato del controllo della firma. SignTool restituisce inoltre un codice di uscita pari a zero per l'esecuzione riuscita, uno per l'esecuzione non riuscita e due per l'esecuzione completata con avvisi.

Per altre informazioni su [SignTool,](signtool.md)vedere [SignTool.](signtool.md)

 

 



