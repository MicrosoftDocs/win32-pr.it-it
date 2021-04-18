---
description: L'implementazione di questa interfaccia viene fornita come codice di esempio con DirectShow SDK.
ms.assetid: a18fc6b6-f37e-4c87-9150-0504333d33c2
title: Interfaccia IMpeg2PsiParser
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMpeg2PsiParser
api_type:
- COM
api_location: ''
ms.openlocfilehash: 51f0f3373c67da75c50ecc2f6bc234e0351f5dc3
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "106303814"
---
# <a name="impeg2psiparser-interface"></a>Interfaccia IMpeg2PsiParser

L'implementazione di questa interfaccia viene fornita come codice di esempio con DirectShow SDK. Non si tratta di un'API DirectShow supportata.

L' `IMpeg2PsiParser` interfaccia recupera le informazioni specifiche del programma (PSI) dal filtro del parser PSI, fornito in DIRECTSHOW SDK come filtro di esempio. Un'applicazione può utilizzare questo filtro per eseguire il mapping degli ID programma (PID) nel filtro MPEG-2 Demultiplexer.

## <a name="members"></a>Membri

L'interfaccia **IMpeg2PsiParser** eredita dall'interfaccia [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) . **IMpeg2PsiParser** dispone anche di questi tipi di membri:

-   [Metodi](#methods)

### <a name="methods"></a>Metodi

L'interfaccia **IMpeg2PsiParser** dispone di questi metodi.



| Metodo                                                                             | Descrizione                                                                               |
|:-----------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------|
| [**FindRecordProgramMapPid**](/previous-versions/windows/desktop/legacy/dd407137(v=vs.85))         | Trova il PID della tabella di mappa dei programmi (PMT) per un programma, in base al numero di programma.<br/> |
| [**GetCountOfElementaryStreams**](impeg2psiparser-getcountofelementarystreams.md) | Recupera il numero di flussi elementari in un programma specificato.<br/>             |
| [**GetCountOfPrograms**](impeg2psiparser-getcountofprograms.md)                   | Recupera il numero di programmi nel flusso di trasporto.<br/>                      |
| [**GetPatVersionNumber**](impeg2psiparser-getpatversionnumber.md)                 | Recupera il \_ campo del numero di versione dalla tabella di associazione dei programmi (Pat).<br/>  |
| [**GetPmtVersionNumber**](impeg2psiparser-getpmtversionnumber.md)                 | Recupera il \_ campo del numero di versione da un PMT specificato.<br/>                      |
| [**GetRecordElementaryPid**](/previous-versions/windows/desktop/legacy/dd376623(v=vs.85))           | Recupera l'assegnazione PID per un flusso elementare specificato in un programma.<br/>   |
| [**GetRecordProgramMapPid**](/previous-versions/windows/desktop/legacy/dd376624(v=vs.85))           | Recupera l'assegnazione PID per un valore PMT specificato.<br/>                              |
| [**GetRecordProgramNumber**](impeg2psiparser-getrecordprogramnumber.md)           | Recupera il numero di programma per un programma specificato.<br/>                          |
| [**GetRecordStreamType**](/previous-versions/windows/desktop/legacy/dd376626(v=vs.85))                 | Recupera il tipo di flusso per un flusso elementare specificato in un programma.<br/>      |
| [**GetTransportStreamId**](impeg2psiparser-gettransportstreamid.md)               | Recupera il \_ \_ campo ID del flusso di trasporto da Pat.<br/>                        |



 

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Esempio di filtro del parser PSI](psi-parser-filter-sample.md)
</dt> </dl>

 

 
