---
description: Contiene informazioni su un modulo di stampa localizzabile.
ms.assetid: 5cc11a77-2b9d-44a4-88de-6ed0b7460bc8
title: FORM_INFO_2 struttura (Winspool.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FORM_INFO_2
- _FORM_INFO_2A
- _FORM_INFO_2W
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: fd933bf0ace6f394a801ab8dc4ef1fa30344b47966c09865a3aa4b713c6f2ed6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118971520"
---
# <a name="form_info_2-structure"></a>Struttura \_ INFO \_ MODULO 2

Contiene informazioni su un modulo di stampa localizzabile.

## <a name="syntax"></a>Sintassi


```C++
typedef struct _FORM_INFO_2 {
  DWORD   Flags;
  LPTSTR  pName;
  SIZEL   Size;
  RECTL   ImageableArea;
  LPCSTR  pKeyword;
  DWORD   StringType;
  LPCTSTR pMuiDll;
  DWORD   dwResourceId;
  LPCTSTR pDisplayName;
  LANGID  wLangId;
} FORM_INFO_2, *PFORM_INFO_2;
```



## <a name="members"></a>Members

<dl> <dt>

**Flag**
</dt> <dd>

Proprietà del form. I valori seguenti sono definiti, ma è possibile impostarne solo uno. Quando il **modulo \_ INFO \_ 2** viene restituito da [**GetForm**](getform.md) o [**EnumForms,**](enumforms.md) **Flags** viene impostato sul valore corrente nel database forms.



| Valore         | Significato                                                                                                                                                                                                                                                                                  |
|---------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| UTENTE \_ DEL MODULO    | Se questo flag di bit è impostato, il modulo è stato definito dall'utente. I moduli con questo flag impostato vengono definiti nel Registro di sistema.                                                                                                                                                                    |
| FORM \_ BUILTIN | Se questo flag di bit è impostato, il modulo fa parte dello spooler. Le definizioni dei moduli con questo flag impostato non vengono visualizzate nel Registro di sistema. I moduli predefiniti non possono essere modificati, pertanto questo flag non deve essere impostato quando la struttura viene passata a [**AddForm**](addform.md) o [**SetForm**](setform.md). |
| STAMPANTE \_ DEL MODULO | Se questo flag di bit è impostato, il modulo è associato a una determinata stampante e la relativa definizione viene visualizzata nel Registro di sistema.                                                                                                                                                                      |



 

</dd> <dt>

**Pname**
</dt> <dd>

Puntatore a una stringa con terminazione Null che specifica il nome del formato. Il nome del modulo non può superare i 31 caratteri.

</dd> <dt>

**Dimensioni**
</dt> <dd>

Larghezza e altezza del modulo in migliaia di millimetri.

</dd> <dt>

**ImageableArea**
</dt> <dd>

Larghezza e altezza, in migliaia di millimetri, dell'area della pagina su cui la stampante può stampare.

</dd> <dt>

**pKeyword**
</dt> <dd>

Puntatore a un identificatore di stringa non localizzabile del formato. Quando viene passato [**a AddForm**](addform.md) o [**SetForm,**](setform.md)questo consente al chiamante di identificare il modulo in tutte le impostazioni locali.

</dd> <dt>

**StringType**
</dt> <dd>

Specifica come viene ottenuto un nome visualizzato localizzato per il form in fase di esecuzione. Vengono definiti i valori seguenti. In una determinata chiamata a [**AddForm**](addform.md) o SetForm è possibile impostarne [**una sola.**](setform.md) È possibile impostare sia STRING MUIDLL che STRING LANGPAIR nel formato \_ \_ INFO **\_ \_ 2** (s) restituito da [**GetForm**](getform.md) o [**EnumForms.**](enumforms.md) Vedere la sezione Osservazioni.



| Valore            | Significato                                                                                                                                                                                        |
|------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| STRINGA \_ NONE     | Non è presente alcun nome visualizzato localizzato.                                                                                                                                                            |
| \_MUIDLL DI STRINGA   | Il nome visualizzato viene estratto dalla DLL [interfaccia utente multilingue](/windows/desktop/Intl/mui-resource-management) risorse localizzate specificata in **pMuiDll**. L'ID si trova nel **membro dwResourceId.** |
| STRINGA \_ LANGPAIR | Il nome visualizzato e l'ID lingua vengono forniti direttamente da **pDisplayName** e la lingua viene specificata da **wLangId**.                                                                       |



 

</dd> <dt>

**pMuiDll**
</dt> <dd>

La [interfaccia utente multilingue](/windows/desktop/Intl/mui-resource-management) DLL della risorsa localizzata che contiene il nome visualizzato localizzato.

</dd> <dt>

**dwResourceId**
</dt> <dd>

ID risorsa del nome visualizzato del modulo in **pMuiDll**.

</dd> <dt>

**pDisplayName**
</dt> <dd>

Nome visualizzato del form nella lingua specificata da **wLangId**.

</dd> <dt>

**wLangId**
</dt> <dd>

Lingua di **pDisplayName**.

</dd> </dl>

## <a name="remarks"></a>Commenti

In una chiamata a [**AddForm**](addform.md) o [**SetForm**](setform.md):

-   Se **StringType** è STRING \_ NONE, **pMuiDll** e **pDisplayName** devono essere **NULL** e **dwResourceId** e **wLangId** devono essere 0.
-   Se **StringType** è STRING \_ MUIDLL, **pDisplayName** deve essere **NULL** e **wLangId** deve essere 0.
-   Se **StringType** è STRING \_ LANGPAIR, **pMuiDll** deve essere **NULL** e **dwResourceId** deve essere 0.

Per un **MODULO \_ INFO \_ 2** restituito da una chiamata a [**GetForm**](getform.md) o [**EnumForms**](enumforms.md):

-   Se **StringType** è sia STRING \_ MUIDLL che STRING \_ LANGPAIR, **pMuiDll,** **pDisplayName,** **dwResourceId** e **wLangId** avranno tutti valori validi.
-   Se **StringType** è solo STRING \_ MUIDLL, **pMuiDll** e **dwResourceId** avranno valori validi. **pDisplayName** sarà **NULL** e **wLangId** sarà 0.
-   Se **StringType** è solo STRING \_ LANGPAIR, **pDisplayName** e **wLangId** avranno valori validi. **pMuiDll** sarà **NULL** e **dwResourceId** sarà 0.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                                            |
| Server minimo supportato<br/> | Windows Solo app desktop server 2008 \[\]<br/>                                                      |
| Intestazione<br/>                   | <dl> <dt>Winspool.h (include Windows.h)</dt> </dl> |
| Nomi Unicode e ANSI<br/>   | **\_ FORM \_ INFO \_ 2W** (Unicode) e **\_ FORM INFO \_ \_ 2A** (ANSI)<br/>                                 |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Stampa](printdocs-printing.md)
</dt> <dt>

[Strutture dell'API Spooler di stampa](printing-and-print-spooler-structures.md)
</dt> <dt>

[Interfaccia utente multilingue](/windows/desktop/Intl/mui-resource-management)
</dt> <dt>

[**AddForm**](addform.md)
</dt> <dt>

[**GetForm**](getform.md)
</dt> <dt>

[**EnumForms**](enumforms.md)
</dt> <dt>

[**SetForm**](setform.md)
</dt> </dl>

 

