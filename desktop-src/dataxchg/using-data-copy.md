---
title: Uso della copia dei dati
description: In questo argomento viene fornito un esempio che illustra come inviare informazioni tra due applicazioni.
ms.assetid: 5b37aa75-1208-435b-bf81-3e75f48f27f3
keywords:
- Windows Interfaccia utente,copia dei dati
- copia di dati,esempi
- copia dei dati, WM_COPYDATA messaggio
- WM_COPYDATA messaggio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b231a03a30c578590dabf04d740f917a791a86d0e868d3587ff0b63bf283866f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119730557"
---
# <a name="using-data-copy"></a>Uso della copia dei dati

L'esempio seguente illustra come inviare informazioni tra due applicazioni usando il [**messaggio \_ WM COPYDATA.**](wm-copydata.md)

L'applicazione mittente visualizza una finestra di dialogo per l'utente che richiede determinate informazioni. L'applicazione include le informazioni in una struttura di dati privata, include un puntatore alla struttura nella struttura [**COPYDATASTRUCT**](/windows/win32/api/winuser/ns-winuser-copydatastruct) e invia le informazioni all'applicazione ricevente usando il [**messaggio WM \_ COPYDATA.**](wm-copydata.md) L'applicazione ricevente ha una finestra nascosta con il nome di classe Disp32Class.


```C++
// ************ Globals ************
//
#define MYDISPLAY 1
typedef struct tagMYREC
{
   char  s1[80];
   char  s2[80];
   DWORD n;
} MYREC;
COPYDATASTRUCT MyCDS;
MYREC MyRec;
HRESULT hResult;
BOOL CALLBACK InfoDlgProc( HWND, UINT, WPARAM, LPARAM );
// ************ Code fragment ****************
// Get data from user. InfoDlgProc stores the information in MyRec.
//
   DialogBox( ghInstance, "InfoDlg", hWnd, (DLGPROC) InfoDlgProc );
//
// Copy data into structure to be passed via WM_COPYDATA.
// Also, we assume that truncation of the data is acceptable.
//
   hResult = StringCbCopy( MyRec.s1, sizeof(MyRec.s1), szFirstName );
   if (hResult != S_OK)
        return False;
   hResult = StringCbCopy( MyRec.s2, sizeof(MyRec.s2), szLastName );
   if (hResult != S_OK)
        return False;
   MyRec.n = nAge;
//
// Fill the COPYDATA structure
// 
   MyCDS.dwData = MYPRINT;          // function identifier
   MyCDS.cbData = sizeof( MyRec );  // size of data
   MyCDS.lpData = &MyRec;           // data structure
//
// Call function, passing data in &MyCDS
//
   hwDispatch = FindWindow( "Disp32Class", "Hidden Window" );
   if( hwDispatch != NULL )
      SendMessage( hwDispatch,
                   WM_COPYDATA,
                   (WPARAM)(HWND) hWnd,
                   (LPARAM) (LPVOID) &MyCDS );
   else
      MessageBox( hWnd, "Can't send WM_COPYDATA", "MyApp", MB_OK );
```



L'applicazione ricevente ha una finestra nascosta che riceve le informazioni da [**WM \_ COPYDATA**](wm-copydata.md) e le visualizza all'utente.


```C++
// ************ Globals ************
//
#define MYDISPLAY 1
typedef struct tagMYREC
{
   char  s1[80];
   char  s2[80];
   DWORD n;
} MYREC;
PCOPYDATASTRUCT pMyCDS;
void WINAPI MyDisplay( LPSTR, LPSTR, DWORD );
//
// ************ Code fragment ****************
//
case WM_COPYDATA:
   pMyCDS = (PCOPYDATASTRUCT) lParam;
   switch( pMyCDS->dwData )
   {
      case MYDISPLAY:
         MyDisplay( (LPSTR) ((MYREC *)(pMyCDS->lpData))->s1,
                    (LPSTR) ((MYREC *)(pMyCDS->lpData))->s2,
                    (DWORD) ((MYREC *)(pMyCDS->lpData))->n );
   }
   break;
```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

**Riferimento**
</dt> <dt>

[**FindWindow**](/windows/desktop/api/winuser/nf-winuser-findwindowa)
</dt> </dl>

 

 