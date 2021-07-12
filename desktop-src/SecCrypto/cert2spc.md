---
description: Cert2SPC
ms.assetid: d05df388-c19d-47a5-9ede-11cf06c29fc8
title: Cert2SPC
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 419f0e6dc6f1183252f138029dadc7817ac3b5ed
ms.sourcegitcommit: 822413efb4a70dd464e5db4d9e8693ef74f8132f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/09/2021
ms.locfileid: "113581979"
---
# <a name="cert2spc"></a>Cert2SPC

Lo strumento Cert2SPC crea un certificato [*SPC (Software Publisher Certificate)*](../secgloss/s-gly.md) di test usando i [*certificati X.509*](../secgloss/x-gly.md) [*esistenti.*](../secgloss/c-gly.md) Cert2SPC può eseguire il wrapping di più certificati X.509 in un oggetto dati [*firmato PKCS \# 7.*](../secgloss/p-gly.md) Lo strumento viene installato nella cartella Bin del percorso di \\ installazione di Microsoft Windows Software Development Kit (SDK).

Cert2SPC è disponibile come parte di Windows SDK, che è possibile scaricare da <https://go.microsoft.com/fwlink/p/?linkid=84091> .

> [!Note]
> Questo strumento è solo a scopo di test. Un SPC valido viene ottenuto da [*un'autorità di certificazione*](../secgloss/c-gly.md).


**Cert2SPC** *Cert1.cer Cert2.cer* ... *Output.spc*

 



| Parametri              | Descrizione                                                                                                                        |
|-------------------------|------------------------------------------------------------------------------------------------------------------------------------|
| *Cert1.cer Cert2.cer* ... | Nomi dei certificati X.509 da includere in SPC. Ogni nome di certificato termina con l'estensione cer.                         |
| *Output.spc*            | Nome dell'oggetto PKCS \# 7 che contiene i certificati X.509 da creare. Il nome del file di output termina con l'estensione spc. |



 

 

 
