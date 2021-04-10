---
description: Contiene informazioni su un modulo di stampa localizzabile.
ms.assetid: 5cc11a77-2b9d-44a4-88de-6ed0b7460bc8
title: Struttura FORM_INFO_2 (winspool. h)
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
ms.openlocfilehash: 6e2129f9776706ce331677e75c5d9c81d82393c6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104227347"
---
# <a name="form_info_2-structure"></a>\_Struttura info modulo \_ 2

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

Proprietà del form. Sono definiti i valori seguenti, ma è possibile impostarne solo uno. Quando il **modulo \_ info \_ 2** viene restituito da [**GetForm**](getform.md) o [**EnumForms**](enumforms.md), **Flags** viene impostato sul valore corrente nel database dei moduli.



| Valore         | Significato                                                                                                                                                                                                                                                                                  |
|---------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| utente del modulo \_    | Se viene impostato questo flag di bit, il form è stato definito dall'utente. I form con questo set di flag sono definiti nel registro di sistema.                                                                                                                                                                    |
| MODULO \_ incorporato | Se viene impostato questo flag di bit, il form fa parte dello spooler. Le definizioni dei moduli con questo set di flag non vengono visualizzate nel registro di sistema. Non è possibile modificare i moduli predefiniti, pertanto non è necessario impostare questo flag quando la struttura viene passata a [**AddForm**](addform.md) o a [**form**](setform.md). |
| \_stampante modulo | Se viene impostato questo flag di bit, il form è associato a una determinata stampante e la relativa definizione viene visualizzata nel registro di sistema.                                                                                                                                                                      |



 

</dd> <dt>

**pName**
</dt> <dd>

Puntatore a una stringa con terminazione null che specifica il nome del form. Il nome del modulo non può superare i 31 caratteri.

</dd> <dt>

**Dimensioni**
</dt> <dd>

Larghezza e altezza del form, in millesimi di millimetro.

</dd> <dt>

**ImageableArea**
</dt> <dd>

Larghezza e altezza, in millesimi di millimetri, dell'area della pagina in cui la stampante è in grado di stampare.

</dd> <dt>

**pKeyword**
</dt> <dd>

Puntatore a un identificatore di stringa non localizzabile del form. Quando viene passato a [**AddForm**](addform.md) o a [**Subform**](setform.md), questo fornisce al chiamante un mezzo per identificare il form in tutte le impostazioni locali.

</dd> <dt>

**StringType**
</dt> <dd>

Specifica il modo in cui viene ottenuto un nome visualizzato localizzato per il form in fase di esecuzione. Vengono definiti i valori seguenti. È possibile impostare un solo in una determinata chiamata a [**AddForm**](addform.md) o a [**form**](setform.md). Sia \_ la stringa MUIDLL che \_ la stringa LANGPAIR possono essere impostate nel **formato \_ info \_ 2** (s) restituito da [**GetForm**](getform.md) o [**EnumForms**](enumforms.md). Vedere la sezione Osservazioni.



| Valore            | Significato                                                                                                                                                                                        |
|------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| STRINGA \_ None     | Nessun nome visualizzato localizzato.                                                                                                                                                            |
| STRINGA \_ MUIDLL   | Il nome visualizzato viene estratto dalla DLL delle risorse localizzate dell' [interfaccia utente multilingue](/windows/desktop/Intl/mui-resource-management) specificata in **pMuiDll**. L'ID si trova nel membro **dwResourceId** . |
| STRINGA \_ LANGPAIR | Il nome visualizzato e l'ID lingua vengono forniti direttamente da **pDisplayName** e la lingua viene specificata da **wLangId**.                                                                       |



 

</dd> <dt>

**pMuiDll**
</dt> <dd>

DLL di risorse localizzate dell' [interfaccia utente multilingue](/windows/desktop/Intl/mui-resource-management) che contiene il nome visualizzato localizzato.

</dd> <dt>

**dwResourceId**
</dt> <dd>

ID risorsa del nome visualizzato del modulo in **pMuiDll**.

</dd> <dt>

**pDisplayName**
</dt> <dd>

Nome visualizzato del modulo nella lingua specificata da **wLangId**.

</dd> <dt>

**wLangId**
</dt> <dd>

Lingua del **pDisplayName**.

</dd> </dl>

## <a name="remarks"></a>Commenti

In una chiamata a [**AddForm**](addform.md) o a [**form**](setform.md):

-   Se **StringType** è una stringa \_ None, **pMuiDll** e **pDisplayName** devono essere **null** e **dwResourceId** e **wLangId** devono essere 0.
-   Se **StringType** è di stringa \_ MUIDLL, **pDisplayName** deve essere **null** e **wLangId** deve essere 0.
-   Se **StringType** è di stringa \_ LANGPAIR, **pMuiDll** deve essere **null** e **dwResourceId** deve essere 0.

Per un **modulo \_ info \_ 2** restituito da una chiamata a [**GetForm**](getform.md) o [**EnumForms**](enumforms.md):

-   Se **StringType** è la stringa \_ MUIDLL e la stringa \_ LANGPAIR **, pMuiDll**, **pDisplayName**, **dwResourceId** e **wLangId** avranno tutti valori validi.
-   Se **StringType** è \_ solo stringa MUIDLL, **pMuiDll** e **dwResourceId** avranno valori validi. **pDisplayName** sarà **null** e **wLangId** sarà 0.
-   Se **StringType** è \_ solo stringa LANGPAIR, **pDisplayName** e **wLangId** avranno valori validi. **pMuiDll** sarà **null** e **dwResourceId** sarà 0.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                                            |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/>                                                      |
| Intestazione<br/>                   | <dl> <dt>Winspool. h (include Windows. h)</dt> </dl> |
| Nomi Unicode e ANSI<br/>   | **\_ Informazioni sul modulo \_ \_ 2W** (Unicode) e **\_ info del modulo \_ \_ 2a** (ANSI)<br/>                                 |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Stampa](printdocs-printing.md)
</dt> <dt>

[Strutture dell'API spooler di stampa](printing-and-print-spooler-structures.md)
</dt> <dt>

[Interfaccia utente multilingue](/windows/desktop/Intl/mui-resource-management)
</dt> <dt>

[**AddForm**](addform.md)
</dt> <dt>

[**GetForm**](getform.md)
</dt> <dt>

[**EnumForms**](enumforms.md)
</dt> <dt>

[**Diformi**](setform.md)
</dt> </dl>

 

