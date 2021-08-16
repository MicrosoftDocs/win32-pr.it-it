---
description: Questo documento contiene un elenco dei codici di errore definiti dal Windows Imaging Component (WIC).
ms.assetid: 1ded909c-311b-49e3-ba23-b22cd7a77bc6
title: Codici di errore dei codec
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8fb8f3911516f11c4a0614461786d6f94eaf00e038e53babb47d4df595797bdb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118207260"
---
# <a name="codec-error-codes"></a>Codici di errore dei codec

Questo documento contiene un elenco dei codici di errore definiti dal Windows Imaging Component (WIC).

-   [Errori WIC per codice](#wic-errors-by-code)
-   [Errori WIC per valore](#wic-errors-by-value)

## <a name="wic-errors-by-code"></a>Errori WIC per codice

La tabella seguente contiene un elenco dei codici di errore usati dagli ELEMENTI WICAPI ordinati in ordine alfabetico. 

| Codice di errore                                      | Valore di errore                      |
|-------------------------------------------------|----------------------------------|
| WINCODEC \_ ERR \_ INTERROTTO                          | 0x80004004 (E \_ ABORT)            |
| ACCESSO WINCODEC \_ ERR \_ NEGATO                     | 0x80070005 (E \_ ACCESSDENIED)     |
| WINCODEC \_ ERR \_ ALREADYLOCKED                    | 0x88982f0D                       |
| WINCODEC \_ ERR \_ BADHEADER                        | 0x88982f61                       |
| WINCODEC \_ ERR \_ BADIMAGE                         | 0x88982f60                       |
| WINCODEC \_ ERR \_ BADMETADATAHEADER                | 0x88982f63                       |
| WINCODEC \_ ERR \_ BADSTREAMDATA                    | 0x88982f70                       |
| CODEC WINCODEC \_ \_ ERRNOTHUMBNAIL                 | 0x88982f44                       |
| WINCODEC \_ ERR \_ CODECPRESENT                     | 0x88982f43                       |
| WINCODEC \_ ERR \_ CODECTOOMANYSCANLINES            | 0x88982f46                       |
| WINCODEC \_ ERR \_ COMPONENTINITIALIZEFAILURE       | 0x88982f8B                       |
| COMPONENTE WINCODEC \_ \_ ERRNOTFOUND                | 0x88982f50                       |
| WINCODEC \_ ERR \_ DUPLICATEMETADATAPRESENT         | 0x88982f8D                       |
| WINCODEC \_ ERR \_ FRAMEMISSING                     | 0x88982f62                       |
| ERRORE GENERICO \_ WINCODEC \_ \_ ERR                   | 0x80004005 (E \_ FAIL)             |
| WINCODEC \_ ERR \_ IMAGESIZEOUTOFRANGE              | 0x88982f51                       |
| WINCODEC \_ ERR \_ INSUFFICIENTBUFFER               | 0x88982f8C                       |
| WINCODEC \_ ERR \_ INTERNALERROR                    | 0x88982f48                       |
| WINCODEC \_ ERR \_ INVALIDPARAMETER                 | 0x80070057 (E \_ INVALIDARG)       |
| WINCODEC \_ ERR \_ INVALIDQUERYCHARACTER            | 0x88982f93                       |
| WINCODEC \_ ERR \_ INVALIDQUERYREQUEST              | 0x88982f90                       |
| WINCODEC \_ ERR \_ INVALIDREGISTRATION              | 0x88982f8A                       |
| WINCODEC \_ ERR \_ NOTIMPLEMENTED                   | 0x80004001 (E \_ NOTIMPL)          |
| WINCODEC \_ ERR \_ NON INIZIALIZZATO                   | 0x88982f0C                       |
| WINCODEC \_ ERR \_ OUTOFMEMORY                      | 0x8007000E (E \_ OUTOFMEMORY)      |
| WINCODEC \_ ERR \_ PALETTEUNAVAILABLE               | 0x88982f45                       |
| WINCODEC \_ ERR \_ PROPERTYNOTFOUND                 | 0x88982f40                       |
| WINCODEC \_ ERR \_ PROPERTYNOTSUPPORTED             | 0x88982f41                       |
| WINCODEC \_ ERR \_ PROPERTYSIZE                     | 0x88982f42                       |
| PROPRIETÀ \_ WINCODEC \_ ERRUNEXPECTEDTYPE           | 0x88982f8E                       |
| WINCODEC \_ ERR \_ REQUESTONLYVALIDATMETADATAROOT   | 0x88982f92                       |
| WINCODEC \_ ERR \_ SOURCERECTDOESNOTMATCHDIMENSIONS | 0x88982f49                       |
| WINCODEC \_ ERR \_ STREAMWRITE                      | 0x88982f71                       |
| WINCODEC \_ ERR \_ STREAMREAD                       | 0x88982f72                       |
| WINCODEC \_ ERR \_ STREAMNOTAVAILABLE               | 0x88982f73                       |
| WINCODEC \_ ERR \_ TOOMUCHMETADATA                  | 0x88982f52                       |
| WINCODEC \_ ERR \_ UNKNOWNIMAGEFORMAT               | 0x88982f07                       |
| WINCODEC \_ ERR \_ UNEXPECTEDMETADATATYPE           | 0x88982f91                       |
| WINCODEC \_ ERR \_ UNEXPECTEDSIZE                   | 0x88982f8F                       |
| WINCODEC \_ ERR \_ UNSUPPORTEDOPERATION             | 0x88982f81                       |
| WINCODEC \_ ERR \_ UNSUPPORTEDPIXELFORMAT           | 0x88982f80                       |
| WINCODEC \_ ERR \_ UNSUPPORTEDVERSION               | 0x88982f0B                       |
| WINCODEC \_ ERR \_ VALUEOUTOFRANGE                  | 0x88982f05                       |
| WINCODEC \_ ERR \_ VALUEOVERFLOW                    | OVERFLOW \_ \_ ARITMETICO E INTSAFE \_ |
| WINCODEC \_ ERR \_ WRONGSTATE                       | 0x88982f04                       |



 

## <a name="wic-errors-by-value"></a>Errori WIC per valore

La tabella seguente contiene un elenco dei codici di errore usati dai WICAPI ordinati in ordine numerico. 

| Codice di errore                       | Valore di errore                                     |
|----------------------------------|-------------------------------------------------|
| 0x80004005 (E \_ FAIL)             | ERRORE GENERICO \_ WINCODEC \_ \_ ERR                   |
| 0x80070057 (E \_ INVALIDARG)       | WINCODEC \_ ERR \_ INVALIDPARAMETER                 |
| 0x8007000E (E \_ OUTOFMEMORY)      | WINCODEC \_ ERR \_ OUTOFMEMORY                      |
| 0x80004001 (E \_ NOTIMPL)          | WINCODEC \_ ERR \_ NOTIMPLEMENTED                   |
| 0x80004004 (E \_ ABORT)            | WINCODEC \_ ERR \_ INTERROTTO                          |
| 0x80070005 (E \_ ACCESSDENIED)     | ACCESSO WINCODEC \_ ERR \_ NEGATO                     |
| OVERFLOW \_ \_ ARITMETICO E INTSAFE \_ | WINCODEC \_ ERR \_ VALUEOVERFLOW                    |
| 0x88982f04                       | WINCODEC \_ ERR \_ WRONGSTATE                       |
| 0x88982f05                       | WINCODEC \_ ERR \_ VALUEOUTOFRANGE                  |
| 0x88982f07                       | WINCODEC \_ ERR \_ UNKNOWNIMAGEFORMAT               |
| 0x88982f0B                       | WINCODEC \_ ERR \_ UNSUPPORTEDVERSION               |
| 0x88982f0C                       | WINCODEC \_ ERR \_ NON INIZIALIZZATO                   |
| 0x88982f0D                       | WINCODEC \_ ERR \_ ALREADYLOCKED                    |
| 0x88982f40                       | WINCODEC \_ ERR \_ PROPERTYNOTFOUND                 |
| 0x88982f41                       | WINCODEC \_ ERR \_ PROPERTYNOTSUPPORTED             |
| 0x88982f42                       | WINCODEC \_ ERR \_ PROPERTYSIZE                     |
| 0x88982f43                       | WINCODEC \_ ERR \_ CODECPRESENT                     |
| 0x88982f44                       | CODEC WINCODEC \_ \_ ERRNOTHUMBNAIL                 |
| 0x88982f45                       | WINCODEC \_ ERR \_ PALETTEUNAVAILABLE               |
| 0x88982f46                       | WINCODEC \_ ERR \_ CODECTOOMANYSCANLINES            |
| 0x88982f48                       | WINCODEC \_ ERR \_ INTERNALERROR                    |
| 0x88982f49                       | WINCODEC \_ ERR \_ SOURCERECTDOESNOTMATCHDIMENSIONS |
| 0x88982f50                       | COMPONENTE WINCODEC \_ \_ ERRNOTFOUND                |
| 0x88982f51                       | WINCODEC \_ ERR \_ IMAGESIZEOUTOFRANGE              |
| 0x88982f52                       | WINCODEC \_ ERR \_ TOOMUCHMETADATA                  |
| 0x88982f60                       | WINCODEC \_ ERR \_ BADIMAGE                         |
| 0x88982f61                       | WINCODEC \_ ERR \_ BADHEADER                        |
| 0x88982f62                       | WINCODEC \_ ERR \_ FRAMEMISSING                     |
| 0x88982f63                       | WINCODEC \_ ERR \_ BADMETADATAHEADER                |
| 0x88982f70                       | WINCODEC \_ ERR \_ BADSTREAMDATA                    |
| 0x88982f71                       | WINCODEC \_ ERR \_ STREAMWRITE                      |
| 0x88982f72                       | WINCODEC \_ ERR \_ STREAMREAD                       |
| 0x88982f73                       | WINCODEC \_ ERR \_ STREAMNOTAVAILABLE               |
| 0x88982f80                       | WINCODEC \_ ERR \_ UNSUPPORTEDPIXELFORMAT           |
| 0x88982f81                       | WINCODEC \_ ERR \_ UNSUPPORTEDOPERATION             |
| 0x88982f8A                       | WINCODEC \_ ERR \_ INVALIDREGISTRATION              |
| 0x88982f8B                       | WINCODEC \_ ERR \_ COMPONENTINITIALIZEFAILURE       |
| 0x88982f8C                       | WINCODEC \_ ERR \_ INSUFFICIENTBUFFER               |
| 0x88982f8D                       | WINCODEC \_ ERR \_ DUPLICATEMETADATAPRESENT         |
| 0x88982f8E                       | PROPRIETÀ \_ WINCODEC \_ ERRUNEXPECTEDTYPE           |
| 0x88982f8F                       | WINCODEC \_ ERR \_ UNEXPECTEDSIZE                   |
| 0x88982f90                       | WINCODEC \_ ERR \_ INVALIDQUERYREQUEST              |
| 0x88982f91                       | WINCODEC \_ ERR \_ UNEXPECTEDMETADATATYPE           |
| 0x88982f92                       | WINCODEC \_ ERR \_ REQUESTONLYVALIDATMETADATAROOT   |
| 0x88982f93                       | WINCODEC \_ ERR \_ INVALIDQUERYCHARACTER            |



 

 

 



