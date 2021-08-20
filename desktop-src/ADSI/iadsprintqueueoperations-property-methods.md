---
title: Metodi della proprietà IADsPrintQueueOperations (Iads.h)
description: I metodi di proprietà dell'interfaccia IADsPrintQueueOperations leggono e scrivono le proprietà elencate nell'elenco seguente. Per altre informazioni sui metodi di proprietà, vedere Metodi delle proprietà di interfaccia.
ms.assetid: a4e6bac5-5d52-4492-b48e-f051fec6158c
ms.tgt_platform: multiple
keywords:
- Metodi della proprietà IADsPrintQueueOperations ADSI
topic_type:
- apiref
api_name:
- IADsPrintQueueOperations Property Methods
- IADsPrintQueueOperations.Status
- IADsPrintQueueOperations.get_Name
- IADsPrintQueueOperations.put_Name
api_location:
- Activeds.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 79c0438491cb62d56584106d78f7639439d93d105fb635eeba0271759247f595
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117839761"
---
# <a name="iadsprintqueueoperations-property-methods"></a>Metodi della proprietà IADsPrintQueueOperations

I metodi di proprietà [**dell'interfaccia IADsPrintQueueOperations**](/windows/desktop/api/Iads/nn-iads-iadsprintqueueoperations) leggono e scrivono le proprietà elencate nell'elenco seguente. Per altre informazioni sui metodi di proprietà, vedere [Metodi delle proprietà di interfaccia.](interface-property-methods.md)

## <a name="properties"></a>Proprietà

<dl> <dt>

**Status**
</dt> <dd> <dl>

Stato corrente delle operazioni della coda di stampa. I valori validi per il codice di stato sono elencati nell'elenco seguente.

<dt>

<span id="ADS_PRINTER_PAUSED"></span><span id="ads_printer_paused"></span>

**Servizi di dominio Active Directory \_ PRINTER \_ PAUSED** (0x00000001)


</dt> <dd></dd> <dt>

<span id="ADS_PRINTER_PENDING_DELETION"></span><span id="ads_printer_pending_deletion"></span>

**Servizi di dominio Active Directory \_ ELIMINAZIONE \_ STAMPANTE \_ IN SOSPESO** (0x00000002)


</dt> <dd></dd> <dt>

<span id="ADS_PRINTER_ERROR"></span><span id="ads_printer_error"></span>

**Servizi di dominio Active Directory \_ ERRORE \_ STAMPANTE** (0x00000003)


</dt> <dd></dd> <dt>

<span id="ADS_PRINTER_PAPER_JAM"></span><span id="ads_printer_paper_jam"></span>

**Servizi di dominio Active Directory \_ \_INCEPPAMENTO CARTA \_** STAMPANTE (0x00000004)


</dt> <dd></dd> <dt>

<span id="ADS_PRINTER_PAPER_OUT"></span><span id="ads_printer_paper_out"></span>

**Servizi di dominio Active Directory \_ PRINTER \_ PAPER \_ OUT** (0x00000005)


</dt> <dd></dd> <dt>

<span id="ADS_PRINTER_MANUAL_FEED"></span><span id="ads_printer_manual_feed"></span>

**Servizi di dominio Active Directory \_ ALIMENTAZIONE \_ MANUALE \_ STAMPANTE** (0x00000006)


</dt> <dd></dd> <dt>

<span id="ADS_PRINTER_PAPER_PROBLEM"></span><span id="ads_printer_paper_problem"></span>

**Servizi di dominio Active Directory \_ PROBLEMA \_ RELATIVO \_ ALLA CARTA** DELLA STAMPANTE (0x00000007)


</dt> <dd></dd> <dt>

<span id="ADS_PRINTER_OFFLINE"></span><span id="ads_printer_offline"></span>

**Servizi di dominio Active Directory \_ PRINTER \_ OFFLINE** (0x00000008)


</dt> <dd></dd> <dt>

<span id="ADS_PRINTER_IO_ACTIVE"></span><span id="ads_printer_io_active"></span>

**Servizi di dominio Active Directory \_ PRINTER \_ IO \_ ACTIVE** (0x00000100)


</dt> <dd></dd> <dt>

<span id="ADS_PRINTER_BUSY"></span><span id="ads_printer_busy"></span>

**Servizi di dominio Active Directory \_ PRINTER \_ BUSY** (0x00000200)


</dt> <dd></dd> <dt>

<span id="ADS_PRINTER_PRINTING"></span><span id="ads_printer_printing"></span>

**Servizi di dominio Active Directory \_ STAMPA \_ DI STAMPANTI** (0x00000400)


</dt> <dd></dd> <dt>

<span id="ADS_PRINTER_OUTPUT_BIN_FULL"></span><span id="ads_printer_output_bin_full"></span>

**Servizi di dominio Active Directory \_ PRINTER \_ OUTPUT \_ BIN \_ FULL** (0x00000800)


</dt> <dd></dd> <dt>

<span id="ADS_PRINTER_NOT_AVAILABLE"></span><span id="ads_printer_not_available"></span>

**Servizi di dominio Active Directory \_ PRINTER \_ NOT \_ AVAILABLE** (0x00001000)


</dt> <dd></dd> <dt>

<span id="ADS_PRINTER_WAITING"></span><span id="ads_printer_waiting"></span>

**Servizi di dominio Active Directory \_ PRINTER \_ WAITING** (0x00002000)


</dt> <dd></dd> <dt>

<span id="ADS_PRINTER_PROCESSING"></span><span id="ads_printer_processing"></span>

**Servizi di dominio Active Directory \_ ELABORAZIONE \_ STAMPANTI** (0x00004000)


</dt> <dd></dd> <dt>

<span id="ADS_PRINTER_INITIALIZING"></span><span id="ads_printer_initializing"></span>

**Servizi di dominio Active Directory \_ INIZIALIZZAZIONE \_ STAMPANTE** (0x00008000)


</dt> <dd></dd> <dt>

<span id="ADS_PRINTER_WARMING_UP"></span><span id="ads_printer_warming_up"></span>

**Servizi di dominio Active Directory \_ RISCALDAMENTO \_ DELLA \_ STAMPANTE** (0x00010000)


</dt> <dd></dd> <dt>

<span id="ADS_PRINTER_TONER_LOW"></span><span id="ads_printer_toner_low"></span>

**Servizi di dominio Active Directory \_ PRINTER \_ TONER \_ LOW** (0x00020000)


</dt> <dd></dd> <dt>

<span id="ADS_PRINTER_NO_TONER"></span><span id="ads_printer_no_toner"></span>

**Servizi di dominio Active Directory \_ PRINTER \_ NO \_ TONER** (0x00040000)


</dt> <dd></dd> <dt>

<span id="ADS_PRINTER_PAGE_PUNT"></span><span id="ads_printer_page_punt"></span>

**Servizi di dominio Active Directory \_ PRINTER \_ PAGE \_ PUNT** (0x00080000)


</dt> <dd></dd> <dt>

<span id="ADS_PRINTER_USER_INTERVENTION"></span><span id="ads_printer_user_intervention"></span>

**Servizi di dominio Active Directory \_ INTERVENTO \_ \_ DELL'UTENTE** DELLA STAMPANTE (0x00100000)


</dt> <dd></dd> <dt>

<span id="ADS_PRINTER_OUT_OF_MEMORY"></span><span id="ads_printer_out_of_memory"></span>

**Servizi di dominio Active Directory \_ MEMORIA \_ \_ INSUFFICIENTE DELLA \_ STAMPANTE** (0x00200000)


</dt> <dd></dd> <dt>

<span id="ADS_PRINTER_DOOR_OPEN"></span><span id="ads_printer_door_open"></span>

**Servizi di dominio Active Directory \_ PRINTER \_ DOOR \_ OPEN** (0x00400000)


</dt> <dd></dd> <dt>

<span id="ADS_PRINTER_SERVER_UNKNOWN"></span><span id="ads_printer_server_unknown"></span>

**Servizi di dominio Active Directory \_ SERVER \_ \_ STAMPANTI SCONOSCIUTO** (0x00800000)


</dt> <dd></dd> <dt>

<span id="ADS_PRINTER_POWER_SAVE"></span><span id="ads_printer_power_save"></span>

**Servizi di dominio Active Directory \_ RISPARMIO \_ ENERGIA \_ STAMPANTE** (0x01000000)


</dt> <dd></dd> </dl> <dt>

Tipo di accesso: Lettura/scrittura
</dt> <dt>

Tipo di dati di scripting: **LONG**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Name(
  [out] LONG* pbstrName
);
HRESULT put_Name(
  [in] LONG bstrName
);
```


</dt> </dl> </dd> </dl>

 

## <a name="examples"></a>Esempio

Nell'esempio Visual Basic codice seguente viene verificato che una stampante sia in stato di inceppamento.


```VB
Dim pqo As IADsPrintQueueOperations
Set pqo = GetObject("WinNT://aMachine/aPrinter")
If pqo.Status = ADS_PRINTER_PAPER_JAM Then
MsgBox "Your printer is jammed."
End If
```



L'esempio di codice C++ seguente verifica che una stampante sia inceppata.


```C++
IADsPrintQueueOperations *pqo;
HRESULT hr = ADsGetObject(L"WinNT://aMachine/aPrinter",
IID_IADsPrintQueueOperations,
(void**)&pqo)
long status;
hr = pqo->get_Status(&status);
if(status = ADS_PRINTER_PAPER_JAM) {
printf("Your printer is jammed.\n");
}
hr = pqo->Release();
```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>                                                                    |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                              |
| Intestazione<br/>                   | <dl> <dt>Iads.h</dt> </dl>           |
| DLL<br/>                      | <dl> <dt>Activeds.dll</dt> </dl>     |
| IID<br/>                      | IID \_ IADsPrintQueueOperations è definito come 124BE5C0-156E-11CF-A986-00AA006BC149<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IADsPrintQueue**](/windows/desktop/api/Iads/nn-iads-iadsprintqueue)
</dt> <dt>

[**IADsPrintQueueOperations**](/windows/desktop/api/Iads/nn-iads-iadsprintqueueoperations)
</dt> </dl>

 

 





