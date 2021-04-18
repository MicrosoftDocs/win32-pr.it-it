---
description: Definisce le modalità di mapping a un ID di classe.
ms.assetid: 1af170e3-1edd-411f-acba-d4b244107996
title: Enumerazione TYSPEC
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- TYSPEC
api_type:
- IDLDef
api_location:
- Wtypes.idl
ms.openlocfilehash: b4c8cf38a8f99458e76cabc726aa39ad01a71ebc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324439"
---
# <a name="tyspec-enumeration"></a>Enumerazione TYSPEC

Definisce le modalità di mapping a un ID di classe.

## <a name="syntax"></a>Sintassi


```C++
typedef enum tagTYSPEC { 
  TYSPEC_CLSID,
  TYSPEC_FILEEXT,
  TYSPEC_MIMETYPE,
  TYSPEC_FILENAME,
  TYSPEC_PROGID,
  TYSPEC_PACKAGENAME,
  TYSPEC_OBJECTID
} TYSPEC;
```



## <a name="constants"></a>Costanti

<dl> <dt>

<span id="TYSPEC_CLSID"></span><span id="tyspec_clsid"></span>**TYSPEC \_ CLSID**
</dt> <dd>

CLSID.

</dd> <dt>

<span id="TYSPEC_FILEEXT"></span><span id="tyspec_fileext"></span>**\_FILEEXT TYSPEC**
</dt> <dd>

Estensione di file. Questo valore non è attualmente supportato.

</dd> <dt>

<span id="TYSPEC_MIMETYPE"></span><span id="tyspec_mimetype"></span>**\_MIMETYPE TYSPEC**
</dt> <dd>

Tipo MIME. Questo valore non è attualmente supportato.

</dd> <dt>

<span id="TYSPEC_FILENAME"></span><span id="tyspec_filename"></span>**\_nome file TYSPEC**
</dt> <dd>

Nome file. Questo valore non è attualmente supportato.

</dd> <dt>

<span id="TYSPEC_PROGID"></span><span id="tyspec_progid"></span>**\_ProgID TYSPEC**
</dt> <dd>

PROGID. Questo valore non è attualmente supportato.

</dd> <dt>

<span id="TYSPEC_PACKAGENAME"></span><span id="tyspec_packagename"></span>**TYSPEC \_ PackageName**
</dt> <dd>

Nome del pacchetto. Questo valore non è attualmente supportato.

</dd> <dt>

<span id="TYSPEC_OBJECTID"></span><span id="tyspec_objectid"></span>**\_ObjectID TYSPEC**
</dt> <dd>

ID di oggetto. Questo valore non è attualmente supportato.

</dd> </dl>

## <a name="remarks"></a>Commenti

L'Unione **uCLSSPEC** è definita come segue:

``` syntax
typedef union switch(DWORD tyspec) {
    case TYSPEC_CLSID:
        CLSID clsid;
    case TYSPEC_FILEEXT:
        LPOLESTR pFileExt;
    case TYSPEC_MIMETYPE:
        LPOLESTR pMimeType;
    case TYSPEC_PROGID:
        LPOLESTR pProgId;
    case TYSPEC_FILENAME:
        LPOLESTR pFileName;
    case TYSPEC_PACKAGENAME:
        struct {
        LPOLESTR pPackageName;
        GUID PolicyId;
        } ByName;
    case TYSPEC_OBJECTID:
        struct {
        GUID ObjectId;
        GUID PolicyId;
        } ByObjectId;
} uCLSSPEC;
```

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------|---------------------------------------------------------------------------------------|
| IDL<br/> | <dl> <dt>Wtypes. idl</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Coinstallazione**](/windows/win32/api/objbase/nf-objbase-coinstall)
</dt> </dl>

 

 
