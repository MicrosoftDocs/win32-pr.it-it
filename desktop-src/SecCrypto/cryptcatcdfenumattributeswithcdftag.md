---
description: Enumera gli attributi dei file membro nella sezione CatalogFiles di un file di definizione del catalogo (CDF).
ms.assetid: 056a5186-a37c-4255-aaa5-4c6e60f5392e
title: CryptCATCDFEnumAttributesWithCDFTag (funzione)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CryptCATCDFEnumAttributesWithCDFTag
api_type:
- DllExport
api_location:
- Wintrust.dll
ms.openlocfilehash: bd3c5905c57d234d42cd89d18c2a141c4026250f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104525729"
---
# <a name="cryptcatcdfenumattributeswithcdftag-function"></a>CryptCATCDFEnumAttributesWithCDFTag (funzione)

\[La funzione **CryptCATCDFEnumAttributesWithCDFTag** è disponibile per l'uso nei sistemi operativi specificati nella sezione requisiti. È possibile che in versioni successive sia stata modificata o non sia più disponibile.\]

La funzione **CryptCATCDFEnumAttributesWithCDFTag** enumera gli attributi dei file membro nella sezione **CatalogFiles** di un file di definizione del catalogo (CDF). **CryptCATCDFEnumAttributesWithCDFTag** viene chiamato da [MakeCat](makecat.md).

> [!Note]  
> A questa funzione non è associato alcun file di intestazione o libreria di importazione. Per chiamare questa funzione, è necessario creare un file di intestazione definito dall'utente e utilizzare le funzioni [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) per collegare dinamicamente a Mssign32.dll.

 

## <a name="syntax"></a>Sintassi


```C++
CRYPTCATATTRIBUTE* WINAPI CryptCATCDFEnumAttributesWithCDFTag(
  _In_ CRYPTCATCDF                  *pCDF,
  _In_ LPWSTR                       pwszMemberTag,
  _In_ CRYPTCATMEMBER               *pMember,
  _In_ CRYPTCATATTRIBUTE            *pPrevAttr,
  _In_ PFN_CDF_PARSE_ERROR_CALLBACK pfnParseError
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pCDF* \[ in\]
</dt> <dd>

Puntatore a una struttura [**CRYPTCATCDF**](/windows/win32/api/mscat/ns-mscat-cryptcatcdf) .

</dd> <dt>

*pwszMemberTag* \[ in\]
</dt> <dd>

Puntatore a una stringa con terminazione **null** che identifica il membro del file di catalogo.

</dd> <dt>

*pMember* \[ in\]
</dt> <dd>

Puntatore a una struttura [**CRYPTCATMEMBER**](/windows/win32/api/mscat/ns-mscat-cryptcatmember) che contiene le informazioni sui membri.

</dd> <dt>

*pPrevAttr* \[ in\]
</dt> <dd>

Puntatore a una struttura [**CRYPTCATATTRIBUTE**](/windows/win32/api/mscat/ns-mscat-cryptcatattribute) per un attributo del membro del file nel file CDF a cui punta *pCDF*.

</dd> <dt>

*pfnParseError* \[ in\]
</dt> <dd>

Puntatore a una funzione definita dall'utente per gestire gli errori di analisi del file.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Al termine dell'operazione, questa funzione restituisce un puntatore a una struttura [**CRYPTCATATTRIBUTE**](/windows/win32/api/mscat/ns-mscat-cryptcatattribute) . Se ha esito negativo, la funzione **CryptCATCDFEnumAttributesWithCDFTag** restituisce un puntatore **null** .

## <a name="remarks"></a>Commenti

Questa funzione viene in genere chiamata in un ciclo per enumerare tutti gli attributi del membro del file di catalogo in un CDF. Prima di immettere il ciclo, impostare *pPrevAttr* su **null**. La funzione restituisce un puntatore al primo attributo. Impostare *pPrevAttr* sul valore restituito della funzione per le iterazioni successive del ciclo.

## <a name="examples"></a>Esempio

Nell'esempio seguente viene illustrata la sequenza di assegnazioni corretta per il parametro *pPrevAttr* ( `pAttr` ).


```C++
    CRYPTCATATTRIBUTE   *pAttr;
    CRYPTCATMEMBER      *pMember;
    LPWSTR              pwszMemberTag;
    CRYPTCATCDF         *pCDF;

    pCDF = CryptCATCDFOpen(L"myCDF", NULL);
    

    pMember = NULL;
    pwszMemberTag = NULL;

    while (pwszMemberTag = CryptCATCDFEnumMembersByCDFTagEx(pCDF,
                                                            pwszMemberTag,
                                                            NULL,
                                                            &pMember,
                                                            FALSE,
                                                            NULL))
    {
        pAttr = NULL;

        while (pAttr = CryptCATCDFEnumAttributesWithCDFTag(pCDF,
                                                           pwszMemberTag,
                                                           pMember,
                                                           pAttr,
                                                           DisplayParseError))
        {
            //do something with pAttr
        }

    }

    CryptCATCDFClose(pCDF);
```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop Windows XP\]<br/>                                             |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                    |
| DLL<br/>                      | <dl> <dt>Wintrust.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[MakeCat](makecat.md)
</dt> <dt>

[**CRYPTCATATTRIBUTE**](/windows/win32/api/mscat/ns-mscat-cryptcatattribute)
</dt> <dt>

[**CRYPTCATCDF**](/windows/win32/api/mscat/ns-mscat-cryptcatcdf)
</dt> <dt>

[**CRYPTCATMEMBER**](/windows/win32/api/mscat/ns-mscat-cryptcatmember)
</dt> <dt>

[**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress)
</dt> <dt>

[**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya)
</dt> </dl>

 

 
