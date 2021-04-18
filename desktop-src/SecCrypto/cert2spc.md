---
description: Cert2SPC
ms.assetid: d05df388-c19d-47a5-9ede-11cf06c29fc8
title: Cert2SPC
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1680f8fe426c2e3a62cac0674928a1520b402357
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/05/2021
ms.locfileid: "106320979"
---
# <a name="cert2spc"></a>Cert2SPC

Lo strumento Cert2SPC crea un [*certificato di autore del software*](../secgloss/s-gly.md) di test usando i certificati [*X. 509*](../secgloss/x-gly.md) [](../secgloss/c-gly.md)esistenti. Cert2SPC può eseguire il wrapping di più certificati X. 509 in un oggetto dati con segno [*PKCS \# 7*](../secgloss/p-gly.md) . Lo strumento viene installato nella \\ cartella bin del percorso di installazione di Microsoft Windows Software Development Kit (SDK).

Cert2SPC è disponibile come parte del Windows SDK, da cui è possibile scaricare <https://go.microsoft.com/fwlink/p/?linkid=84091> .

> [!Note]
> Questo strumento è solo a scopo di test. Un SPC valido viene ottenuto da un' [*autorità di certificazione*](../secgloss/c-gly.md).


**Cert2spc** *Cert1. cer Cert2. cer* ... *Output. SPC*

 



|                         |                                                                                                                                    |
|-------------------------|------------------------------------------------------------------------------------------------------------------------------------|
| *Cert1. cer Cert2. cer* ... | Nomi dei certificati X. 509 da includere nel SPC. Ogni nome di certificato termina con l'estensione cer.                         |
| *Output. SPC*            | Nome dell'oggetto PKCS \# 7 che contiene i certificati X. 509 da creare. Il nome del file di output termina con l'estensione SPC. |



 

 

 
