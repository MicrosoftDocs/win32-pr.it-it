---
description: Contiene informazioni per la funzione CryptUIDlgViewSignerInfo.
ms.assetid: 2b76de4f-4b35-477e-a67e-435434e066c6
title: Struttura CRYPTUI_VIEWSIGNERINFO_STRUCT
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
ms.openlocfilehash: da150da6b5115e20a78a4edca64a5c9a97f66132
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104050008"
---
# <a name="cryptui_viewsignerinfo_struct-structure"></a>\_ \_ Struttura struct VIEWSIGNERINFO CRYPTUI

\[La struttura dello **\_ \_ struct VIEWSIGNERINFO CRYPTUI** è disponibile per l'uso nei sistemi operativi specificati nella sezione requisiti. È possibile che in versioni successive sia stata modificata o non sia più disponibile.\]

La struttura **CRYPTUI \_ VIEWSIGNERINFO \_ struct** contiene informazioni per la funzione [**CryptUIDlgViewSignerInfo**](cryptuidlgviewsignerinfo.md) .

> [!Note]  
> Questa struttura non è dichiarata in un file di intestazione pubblicato. Per usare questa struttura, dichiararla nel formato esatto indicato.

 

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

Handle della finestra che deve essere l'elemento padre della finestra di dialogo. Questo membro può essere **null** se la finestra di dialogo non deve avere un elemento padre.

</dd> <dt>

**dwFlags**
</dt> <dd>

Set di flag che modifica il comportamento della funzione [**CryptUIDlgViewSignerInfo**](cryptuidlgviewsignerinfo.md) . Non sono attualmente definiti flag, pertanto il membro deve essere zero.

</dd> <dt>

**szTitle**
</dt> <dd>

Puntatore a una stringa con terminazione null che contiene il titolo da visualizzare nella finestra di dialogo. Se questo membro è **null**, viene utilizzato un titolo predefinito.

</dd> <dt>

**pSignerInfo**
</dt> <dd>

Puntatore a una struttura [**di \_ \_ informazioni sul firmatario CMSG**](/windows/desktop/api/Wincrypt/ns-wincrypt-cmsg_signer_info) che contiene le informazioni sul firmatario da visualizzare.

</dd> <dt>

**hMsg**
</dt> <dd>

Handle del messaggio dal quale sono state estratte le informazioni sul firmatario.

</dd> <dt>

**pszOID**
</dt> <dd>

Puntatore a una stringa ANSI con terminazione null che contiene la rappresentazione di stringa dell' [*identificatore di oggetto*](../secgloss/o-gly.md) (OID) che indica la convalida del certificato per cui è stata effettuata la firma. Se, ad esempio, viene chiamato il metodo per visualizzare la firma di un [*elenco di certificati attendibili*](../secgloss/c-gly.md) (CTL), è necessario passare la stringa OID di **\_ \_ \_ \_ firma utilizzo szOID KP CTL** . Se questo membro è **null**, il certificato non viene convalidato per l'utilizzo.

</dd> <dt>

**dwReserved**
</dt> <dd>

Questo parametro non è attualmente in uso. Questo membro deve essere **null**.

</dd> <dt>

**cStores**
</dt> <dd>

Numero di elementi nella matrice **rghStores** .

</dd> <dt>

**rghStores**
</dt> <dd>

Matrice di valori **HCERTSTORE** che rappresentano gli altri archivi certificati in cui cercare il certificato che ha firmato il messaggio. Se questo membro è **null**, non viene eseguita la ricerca di altri archivi. Il membro **cStores** contiene il numero di elementi in questa matrice.

</dd> <dt>

**cPropSheetPages**
</dt> <dd>

Numero di elementi nella matrice **rgPropSheetPages** .

</dd> <dt>

**rgPropSheetPages**
</dt> <dd>

Matrice di puntatori della struttura [**PROPSHEETPAGE**](/windows/win32/api/prsht/ns-prsht-propsheetpagea_v2) che definiscono le pagine aggiuntive da visualizzare nella finestra di dialogo standard. Se questo membro è **null**, non verrà visualizzata alcuna pagina aggiuntiva. Il membro **cPropSheetPages** contiene il numero di elementi in questa matrice.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop Windows XP\]<br/>                                                               |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                                      |
| Nomi Unicode e ANSI<br/>   | **CRYPTUI \_ VIEWSIGNERINFO \_ STRUCTW** (Unicode) e **CRYPTUI \_ VIEWSIGNERINFO \_ STRUCTA** (ANSI)<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**CryptUIDlgViewSignerInfo**](cryptuidlgviewsignerinfo.md)
</dt> </dl>

 

 
