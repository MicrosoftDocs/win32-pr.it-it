---
description: Contiene informazioni per la funzione CryptUIDlgViewSignerInfo.
ms.assetid: 2b76de4f-4b35-477e-a67e-435434e066c6
title: CRYPTUI_VIEWSIGNERINFO_STRUCT struttura
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CRYPTUI_VIEWSIGNERINFO_STRUCT
- CRYPTUI_VIEWSIGNERINFO_STRUCTA
- CRYPTUI_VIEWSIGNERINFO_STRUCTW
api_type:
- NA
api_location: ''
ms.openlocfilehash: bf35b4475047548e1744174717c238e99c6a744c17ef2fa76ce48217a4fc72aa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119875861"
---
# <a name="cryptui_viewsignerinfo_struct-structure"></a>Struttura STRUCT CRYPTUI \_ \_ VIEWSIGNERINFO

\[La **struttura \_ \_ STRUCT CRYPTUI VIEWSIGNERINFO** è disponibile per l'uso nei sistemi operativi specificati nella sezione Requisiti. È possibile che in versioni successive sia stata modificata o non sia più disponibile.\]

La **struttura \_ \_ STRUCT CRYPTUI VIEWSIGNERINFO** contiene informazioni per la [**funzione CryptUIDlgViewSignerInfo.**](cryptuidlgviewsignerinfo.md)

> [!Note]  
> Questa struttura non è dichiarata in un file di intestazione pubblicato. Per usare questa struttura, dichiararla nel formato esatto illustrato.

 

## <a name="syntax"></a>Sintassi


```C++
typedef struct tagCRYPTUI_VIEWSIGNERINFO_STRUCT {
  DWORD            dwSize;
  HWND             hwndParent;
  DWORD            dwFlags;
  LPCTSTR          szTitle;
  CMSG_SIGNER_INFO *pSignerInfo;
  HCRYPTMSG        hMsg;
  LPCSTR           pszOID;
  DWORD_PTR        dwReserved;
  DWORD            cStores;
  HCERTSTORE       *rghStores;
  DWORD            cPropSheetPages;
  LPCPROPSHEETPAGE rgPropSheetPages;
} CRYPTUI_VIEWSIGNERINFO_STRUCT, *PCRYPTUI_VIEWSIGNERINFO_STRUCT;
```



## <a name="members"></a>Members

<dl> <dt>

**dwSize**
</dt> <dd>

Dimensione, in byte, della struttura.

</dd> <dt>

**hwndParent**
</dt> <dd>

Handle della finestra che deve essere l'elemento padre della finestra di dialogo. Questo membro può essere **NULL se** la finestra di dialogo non deve avere un elemento padre.

</dd> <dt>

**dwFlags**
</dt> <dd>

Set di flag che modifica il comportamento della [**funzione CryptUIDlgViewSignerInfo.**](cryptuidlgviewsignerinfo.md) Non sono attualmente definiti flag, pertanto questo membro deve essere zero.

</dd> <dt>

**szTitle**
</dt> <dd>

Puntatore a una stringa con terminazione Null contenente il titolo da visualizzare nella finestra di dialogo. Se questo membro è **NULL,** viene usato un titolo predefinito.

</dd> <dt>

**pSignerInfo**
</dt> <dd>

Puntatore a una [**struttura CMSG \_ SIGNER \_ INFO**](/windows/desktop/api/Wincrypt/ns-wincrypt-cmsg_signer_info) che contiene le informazioni sul firmatario da visualizzare.

</dd> <dt>

**hMsg**
</dt> <dd>

Handle del messaggio da cui sono stati estratti i dati del firmatario.

</dd> <dt>

**pszOID**
</dt> <dd>

Puntatore a una stringa ANSI con terminazione Null [](../secgloss/o-gly.md) che contiene la rappresentazione di stringa dell'identificatore di oggetto (OID) che indica per quale certificato è stata firmata la firma deve essere convalidato. Ad esempio, se viene chiamato per visualizzare [](../secgloss/c-gly.md) la firma di un elenco di certificati attendibili (CTL), la stringa OID **SzOID \_ \_ KP CTL \_ USAGE \_ SIGNING** deve essere passata. Se questo membro è **NULL,** il certificato non viene convalidato per gli utilizzi.

</dd> <dt>

**dwReserved**
</dt> <dd>

Questo parametro non è attualmente utilizzato. Questo membro deve essere **NULL.**

</dd> <dt>

**cStores**
</dt> <dd>

Numero di elementi nella **matrice rghStores.**

</dd> <dt>

**rghStores**
</dt> <dd>

Matrice di valori **HCERTSTORE** che rappresentano gli altri archivi certificati in cui cercare il certificato che ha firmato il messaggio. Se questo membro è **NULL,** non viene cercata alcuna archiviazione aggiuntiva. Il **membro cStores** contiene il numero di elementi in questa matrice.

</dd> <dt>

**cPropSheetPages**
</dt> <dd>

Numero di elementi nella **matrice rgPropSheetPages.**

</dd> <dt>

**rgPropSheetPages**
</dt> <dd>

Matrice di [**puntatori alla struttura PROPSHEETPAGE**](/windows/win32/api/prsht/ns-prsht-propsheetpagea_v2) che definiscono eventuali pagine aggiuntive da visualizzare nella finestra di dialogo standard. Se questo membro è **NULL,** non verranno visualizzate altre pagine. Il **membro cPropSheetPages** contiene il numero di elementi in questa matrice.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop XP\]<br/>                                                               |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2003 \[\]<br/>                                                      |
| Nomi Unicode e ANSI<br/>   | **CRYPTUI \_ \_STRUCTW VIEWSIGNERINFO** (Unicode) e **CRYPTUI \_ VIEWSIGNERINFO \_ STRUCTA** (ANSI)<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**CryptUIDlgViewSignerInfo**](cryptuidlgviewsignerinfo.md)
</dt> </dl>

 

 
