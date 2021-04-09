---
title: Configurazione di flussi VBR
description: Configurazione di flussi VBR
ms.assetid: 83caabb7-b7fa-4b0a-a608-d5a86e4101b8
keywords:
- flussi, configurazione di flussi VBR
- flussi, velocità in bit variabile (VBR)
- velocità in bit variabile (VBR), flussi
- VBR (velocità in bit variabile), flussi
- flussi, interfaccia IWMPropertyVault
- IWMPropertyVault
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f6667dc9cf66932cf8af90da0b0e59ad27860ab3
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/19/2020
ms.locfileid: "103956182"
---
# <a name="configuring-vbr-streams"></a>Configurazione di flussi VBR

È possibile utilizzare la codifica a velocità in bit variabile (VBR) per produrre flussi di alta qualità per i file locali o per il download e la riproduzione. Sono disponibili tre opzioni per VBR: basata sulla qualità (un passaggio), non vincolato (due passaggi) e vincolato (due passaggi). Per ulteriori informazioni sui tipi di codifica VBR, vedere la pagina relativa alla [codifica con velocità in bit variabile (VBR)](variable-bit-rate--vbr--encoding.md).

È possibile configurare la codifica VBR in un profilo impostando le proprietà con l'interfaccia [**IWMPropertyVault**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmpropertyvault) . Nella tabella seguente vengono descritte le proprietà utilizzate per configurare la codifica VBR.



| Proprietà                     | Descrizione                                                                                       |
|------------------------------|---------------------------------------------------------------------------------------------------|
| **g \_ wszVBREnabled**         | . Impostare su true per utilizzare la codifica VBR.                                                   |
| **g \_ wszVBRQuality**         | Valore **DWORD** . Impostare sul livello di qualità desiderato (da 1 a 100) per la codifica VBR basata sulla qualità.      |
| **g \_ wszVBRBitrateMax**      | Valore **DWORD** . Impostare sulla velocità in bit massima, in bit al secondo, per la codifica VBR vincolata.   |
| **g \_ wszVBRBufferWindowMax** | Valore **DWORD** . Impostare sulla finestra massima del buffer, in millisecondi, per la codifica VBR vincolata. |



 

Le sezioni seguenti descrivono come usare i diversi tipi di codifica della velocità in bit variabile.



| Sezione                                                              | Descrizione                                                                                                        |
|----------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------|
| [Per configurare Quality-Based VBR](to-configure-quality-based-vbr.md) | Viene descritto come usare la codifica della velocità in bit variabile in base a un livello di qualità statico.                                   |
| [Per configurare il VBR non vincolato](to-configure-unconstrained-vbr.md) | Viene descritto come usare la codifica della velocità in bit variabile in base a una velocità in bit media di destinazione senza un valore di picco esplicito. |
| [Per configurare il VBR vincolato](to-configure-constrained-vbr.md)     | Viene descritto come usare la codifica della velocità in bit variabile in base a una velocità in bit media di destinazione e a un valore di picco esplicito.     |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Configurazione di flussi**](configuring-streams.md)
</dt> </dl>

 

 




