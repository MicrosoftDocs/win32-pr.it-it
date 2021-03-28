---
description: Fornisce informazioni ai metodi dell'interfaccia IQueryAssociations.
ms.assetid: e67d0282-9090-43e6-aedf-bb1fc0443221
title: Enumerazione ASSOCF
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 70ddb0b4fb89925c643eb01c276772b9a7151578
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/05/2021
ms.locfileid: "104234549"
---
# <a name="assocf-enumeration"></a>Enumerazione ASSOCF

Fornisce informazioni ai metodi dell'interfaccia [**IQueryAssociations**](/windows/win32/api/shlwapi/nn-shlwapi-iqueryassociations) .

## <a name="syntax"></a>Sintassi

<span codelanguage="ManagedCPlusPlus"></span>

<table><colgroup><col style="width: 100%" /></colgroup><thead><tr class="header"><th>C++</th></tr></thead><tbody><tr class="odd"><td><pre><code>typedef enum  { 
  ASSOCF_NONE                  = 0x00000000,
  ASSOCF_INIT_NOREMAPCLSID     = 0x00000001,
  ASSOCF_INIT_BYEXENAME        = 0x00000002,
  ASSOCF_OPEN_BYEXENAME        = 0x00000002,
  ASSOCF_INIT_DEFAULTTOSTAR    = 0x00000004,
  ASSOCF_INIT_DEFAULTTOFOLDER  = 0x00000008,
  ASSOCF_NOUSERSETTINGS        = 0x00000010,
  ASSOCF_NOTRUNCATE            = 0x00000020,
  ASSOCF_VERIFY                = 0x00000040,
  ASSOCF_REMAPRUNDLL           = 0x00000080,
  ASSOCF_NOFIXUPS              = 0x00000100,
  ASSOCF_IGNOREBASECLASS       = 0x00000200,
  ASSOCF_INIT_IGNOREUNKNOWN    = 0x00000400,
  ASSOCF_INIT_FIXED_PROGID     = 0x00000800,
  ASSOCF_IS_PROTOCOL           = 0x00001000,
  ASSOCF_INIT_FOR_FILE         = 0x00002000
} ASSOCF;</code></pre></td></tr></tbody></table>



## <a name="constants"></a>Costanti

 <span id="ASSOCF_NONE"></span><span id="assocf_none"></span>**ASSOCF \_ None** 

Nessuna delle opzioni seguenti è impostata.

 <span id="ASSOCF_INIT_NOREMAPCLSID"></span><span id="assocf_init_noremapclsid"></span>**ASSOCF \_ init \_ NOREMAPCLSID** 

Indica ai metodi dell'interfaccia [**IQueryAssociations**](/windows/win32/api/shlwapi/nn-shlwapi-iqueryassociations) di non eseguire il mapping dei valori CLSID ai valori ProgID.

 <span id="ASSOCF_INIT_BYEXENAME"></span><span id="assocf_init_byexename"></span>**ASSOCF \_ init \_ BYEXENAME** 

Identifica il valore del parametro *pwszAssoc* di [**IQueryAssociations:: init**](/windows/win32/api/shlwapi/nf-shlwapi-iqueryassociations-init) come nome file eseguibile. Se questo flag non è impostato, la chiave radice verrà impostata sul ProgID associato alla chiave **exe** anziché sul ProgID del file eseguibile.

 <span id="ASSOCF_OPEN_BYEXENAME"></span><span id="assocf_open_byexename"></span>**ASSOCF \_ Open \_ BYEXENAME** 

Identico a **ASSOCF \_ init \_ BYEXENAME**.

 <span id="ASSOCF_INIT_DEFAULTTOSTAR"></span><span id="assocf_init_defaulttostar"></span>**ASSOCF \_ init \_ DEFAULTTOSTAR** 

Specifica che quando un metodo [**IQueryAssociations**](/windows/win32/api/shlwapi/nn-shlwapi-iqueryassociations) non trova il valore richiesto sotto la chiave radice, deve tentare di recuperare il valore confrontabile dalla **\*** sottochiave.

 <span id="ASSOCF_INIT_DEFAULTTOFOLDER"></span><span id="assocf_init_defaulttofolder"></span>**ASSOCF \_ init \_ DEFAULTTOFOLDER** 

Specifica che quando un metodo [**IQueryAssociations**](/windows/win32/api/shlwapi/nn-shlwapi-iqueryassociations) non trova il valore richiesto sotto la chiave radice, deve tentare di recuperare il valore confrontabile dalla sottochiave della **cartella** .

 <span id="ASSOCF_NOUSERSETTINGS"></span><span id="assocf_nousersettings"></span>**\_NOUSERSETTINGS ASSOCF** 

Specifica che deve essere eseguita la ricerca solo nella **\_ \_ radice delle classi HKEY** e che l' **\_ \_ utente corrente di HKEY** deve essere ignorato.

 <span id="ASSOCF_NOTRUNCATE"></span><span id="assocf_notruncate"></span>**ASSOCF \_ NOtruncate** 

Specifica che la stringa restituita non deve essere troncata. Restituire invece un valore di errore e le dimensioni necessarie per la stringa completa.

 <span id="ASSOCF_VERIFY"></span><span id="assocf_verify"></span>**\_Verifica ASSOCF** 

Indica ai metodi [**IQueryAssociations**](/windows/win32/api/shlwapi/nn-shlwapi-iqueryassociations) di verificare che i dati siano accurati. Questa impostazione consente ai metodi **IQueryAssociations** di leggere i dati dal disco rigido dell'utente per la verifica. Ad esempio, è possibile controllare il nome descrittivo nel registro di sistema rispetto a quello archiviato nel file con estensione exe. L'impostazione di questo flag in genere riduce l'efficienza del metodo.

 <span id="ASSOCF_REMAPRUNDLL"></span><span id="assocf_remaprundll"></span>**\_REMAPRUNDLL ASSOCF** 

Indica ai metodi [**IQueryAssociations**](/windows/win32/api/shlwapi/nn-shlwapi-iqueryassociations) di ignorare Rundll.exe e restituire informazioni sulla propria destinazione. In genere i metodi **IQueryAssociations** restituiscono informazioni sul primo file con estensione exe o dll in una stringa di comando. Se un comando USA Rundll.exe, l'impostazione di questo flag indica al metodo di ignorare Rundll.exe e restituire informazioni sulla destinazione.

 <span id="ASSOCF_NOFIXUPS"></span><span id="assocf_nofixups"></span>**\_NOFIXUPS ASSOCF** 

Indica ai metodi [**IQueryAssociations**](/windows/win32/api/shlwapi/nn-shlwapi-iqueryassociations) di non correggere gli errori nel registro di sistema, ad esempio il nome descrittivo di una funzione che non corrisponde a quella presente nel file con estensione exe.

 <span id="ASSOCF_IGNOREBASECLASS"></span><span id="assocf_ignorebaseclass"></span>**\_IGNOREBASECLASS ASSOCF** 

Specifica che il valore di BaseClass deve essere ignorato.

 <span id="ASSOCF_INIT_IGNOREUNKNOWN"></span><span id="assocf_init_ignoreunknown"></span>**ASSOCF \_ init \_ IGNOREUNKNOWN** 

**Introdotta in Windows 7**. Specifica che il ProgID "Unknown" deve essere ignorato. in alternativa, ha esito negativo.

 <span id="ASSOCF_INIT_FIXED_PROGID"></span><span id="assocf_init_fixed_progid"></span>**\_ \_ ProgID fisso ASSOCF \_ init** 

**Introdotta in Windows 8**. Specifica che il ProgID fornito deve essere mappato utilizzando le impostazioni predefinite del sistema, anziché le impostazioni predefinite dell'utente corrente.

 <span id="ASSOCF_IS_PROTOCOL"></span><span id="assocf_is_protocol"></span>**ASSOCF \_ è un \_ protocollo** 

**Introdotta in Windows 8**. Specifica che il valore è un protocollo e deve essere mappato utilizzando le impostazioni predefinite dell'utente corrente.

 <span id="ASSOCF_INIT_FOR_FILE"></span><span id="assocf_init_for_file"></span>**ASSOCF \_ init \_ per \_ file** 

**Introdotta in Windows 8.1**. Specifica che il ProgID corrisponde a un'associazione basata sull'estensione di file. Usare insieme al **\_ \_ \_ ProgID fisso ASSOCF init**.

 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimo supportato | Windows 2000 Professional, \[ solo app desktop Windows XP\]               |
| Server minimo supportato | Windows 2000 Server \[solo app desktop\]                                 |
| Intestazione                   |  Shlwapi. h  |



## <a name="see-also"></a>Vedi anche

 [**AssocQueryKey**](/windows/win32/api/shlwapi/nf-shlwapi-assocquerykeya) [**AssocQueryString**](/windows/win32/api/shlwapi/nf-shlwapi-assocquerystringa) [**AssocQueryStringByKey**](/windows/win32/api/shlwapi/nf-shlwapi-assocquerystringa) 

 

 

© 2017 Microsoft. Tutti i diritti sono riservati.
